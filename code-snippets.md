# Code Snippets

## Admin Storier

## Reports Table - Redo report generation button

```js
<button
    className="btn btn-sm btn-success mr-1 mb-1"
    onClick={() => {
        const testProcessReport = functions.httpsCallable('testProcessReport');
        const result = testProcessReport({
            reportId: row.id
        });
    }}
>
    Test
</button>
```
