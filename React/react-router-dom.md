# React Router DOM

_React Router DOM is a tool that handles routes in a web app using dynamic routing. Dynamic routing takes place as the app is rendering._

```node
npm install react-router-dom
```

## App Setup

## Navigating to a page

### Starting Page

```js
import { Link } from 'react-router-dom'

<Link
    to={{
        pathnoame: "/next-page",
        state: "some-value" // NOTE: You don't have to call it state.
    }}
>
    Link Text
</LinkButton>
```

### Next Page

```jsx
const NextPage = ({location}) => {
    const value = location.state
}
```

## LinkButton

A custom class that allows buttons to be used as Links.

```js
import React from 'react'
import PropTypes from 'prop-types'
import { withRouter } from 'react-router'

const LinkButton = (props) => {
  const {
    history,
    location,
    match,
    staticContext,
    to,
    onClick,
    // ⬆ filtering out props that `button` doesn’t know what to do with.
    ...rest
  } = props
  return (
    <button
      {...rest} // `children` is just another prop!
      onClick={(event) => {
        onClick && onClick(event)
        history.push(to)
      }}
    />
  )
}

LinkButton.propTypes = {
  to: PropTypes.string.isRequired,
  children: PropTypes.node.isRequired
}

export default withRouter(LinkButton)
```