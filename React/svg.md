# SVG Files in React

Find a great tutorial [here](https://blog.logrocket.com/how-to-use-svgs-in-react/).

```js
import ReactLogo from './logo.svg';

const App = () => {
  return (
    <div className="App">
      <img src={ReactLogo} alt="React Logo" />
    </div>
  );
}
```