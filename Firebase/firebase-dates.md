# Firebase Dates

## Date Creation

```js
import firebase from 'firebase'

const date = firebase.firestore.Timestamp.fromDate(new Date())
```

## Read Date

```js
const date = data.date.toDate()
```
