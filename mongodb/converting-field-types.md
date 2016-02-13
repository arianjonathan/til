#Converting Field Types

mongo shell allows supports Javascript, which allows for nifty things like converting a collection's field type.

Convert String field to Integer:
```Javascript
db.db-name.find({field-name: {$exists: true}}).forEach(function(obj) { 
    obj.field-name = new NumberInt(obj.field-name);
    db.db-name.save(obj);
});
```

Convert Integer field to String:
```Javascript
db.db-name.find({field-name: {$exists: true}}).forEach(function(obj) {
    obj.field-name = "" + obj.field-name;
    db.db-name.save(obj);
});
```
