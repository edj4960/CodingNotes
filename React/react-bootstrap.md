# React Bootstrap

## Modal

```jsx
import Modal from 'react-bootstrap/Modal'

<Modal 
show={}
onHide={}
>
    <Modal.Header closeButton>
        {/*Header Content*/}
    </Modal.Header>
    <Modal.Body>
        {/*Body Content*/}
    </Modal.Body>
    <Modal.Footer>
        {/*Footer Content*/}
    </Modal.Footer>
</Modal>
```

## Button

### Importing

There are multiple libraries that provide `<Button/>` :

1. `import { Button } from 'reactstrap'`
2. `import Button from 'react-bootstrap/Button`

### Example

```html
<Button variant="primary">Primary</Button>
```

## [Transitions](https://react-bootstrap.github.io/utilities/transitions/)

### Collapse

```js
const [open, setOpen] = useState(false);

return (
<>
    <Button onClick={() => setOpen(!open)} >click</Button>
    
    <Collapse in={open}>
        {/* Content */}
    </Collapse>
</>
);
```
