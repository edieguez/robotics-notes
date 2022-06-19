# General operators

- $exists

## $exists example

```javascript
db.users.find({
  name: { $exists: true }
})
```
