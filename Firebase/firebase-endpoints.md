# Firebase Endpoints

## Create an http endpoint

```js
const functions = require('firebase-functions');
const { getUser } = require('../firestore/users');

const functionName = functions.https.onCall(async (data, context) => {
    // Getting user who sent request.
    const uid = context.auth.uid;
    const adminUser = await getUser(uid);
    
    // data.param
    return {
        success: true
    }
});

module.exports = {
    functionName
};
```

## Call an endpoint from front end

```js
import { functions } from '../../firebase';

const endpointName = functions.httpsCallable('<endpointName>');

const result = await endpointName({
    <Body>
});
```
