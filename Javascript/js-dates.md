# Javscript Dates

## Formatting using dateformat

### Installation

```js
npm install dateformat
```

### Usage

```js
const dateformat = require('dateformat')
const now = new Date()
dateformat(now, "dddd, mmmm dS, yyyy, h:MM:ss TT")
```

## Manipulation

```js
const new = new Date()
const newDate = now.setDate(now.getDate() + 30);
```
