# Javascript Arrays

## Functions

### Reduce

```js
const initialValue = 0

const value = arr.reduce((accumulator, currentValue, currentIndex, sourceArray) => {
    return // something (usually accumulator +|*|/ currentValue)
}, initialValue)
```

### Map

Returns a new array without affecting the original.

```js
const newArr = arr.map((element, index, array) => {
    return // something
})
```

## Custom Solutions

### Array of Objects to Object

```js
const array = [
    {key:'k1',value:'v1'},
    {key:'k2',value:'v2'},
]
const mapped = array.map(item => ({ [item.key]: item.value }))
const newObj = Object.assign({}, ...mapped);
/*{
    key: value,
    key: value
}*/
```
