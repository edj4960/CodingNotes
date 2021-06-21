# Firestore

## Query Specific Document

```js
const item = (await firestore
    .collection('collectionName')
    .doc('docId')
    .get())
```

## Batch Requests

Batch requests allow you to group post requests to execute at the same time.

```js
const batch = firestore.batch();

// Set
const docRef = firestore.collection("collection").doc("docId");
batch.set(docRef, {});

// Update
const docRef2 = firestore.collection("collection").doc("docId");
batch.update(docRef2, "attribute", newValue);

// Delete
const docRef3 = firestore.collection("collection").doc("docId");
batch.delete(docRef3);

// Commit the batch
batch.commit();
```
