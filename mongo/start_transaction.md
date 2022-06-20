# Start Mongo transaction

```javascript
session = db.getMongo().startSession({readPreference: {mode: 'primary'}})

// Get a transaction
session.startTransaction()

session.getDatabase('sample_mflix').movies.updateMany(
  {},
  {
    $set: {message: 'Transaction ocurred'}
  }
)

// Until you commit the transaction, the changes are not reflected in the database
session.commitTransaction()
session.endSession()
```
