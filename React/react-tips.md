# React Tips

## Parse HTML

Parsing html means taking a string such as `<p>some text</p>` and converting it to display as html.

`npm install react-html-parser`

```jsx
import ReactHtmlParser from 'react-html-parser'

const html = '<p>some text</p>'

<div>
    {ReactHtmlParser(html)}
</div>
```
