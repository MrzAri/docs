---
title: 'delete'
notes:
  - 'Needs example, spec reference, standardization status'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/indexeddb/IDBCursor
    href: /apis/indexeddb/IDBCursor
  return_type:
    predicate: 'Returns an object of type  '
    value: ''
    href: /apis/indexeddb/IDBCursor
summary: 'Returns an IDBRequest object and, in a separate thread, deletes the record at the cursor''s position, without changing the cursor''s position. Once the record is deleted, the cursor''s value is set to null.'
tags:
  - API_Object_Methods
  - API
  - IndexedDB
  - Needs_Examples
uri: apis/indexeddb/IDBCursor/delete

---
## Summary

Returns an IDBRequest object and, in a separate thread, deletes the record at the cursor's position, without changing the cursor's position. Once the record is deleted, the cursor's value is set to null.

Method of [apis/indexeddb/IDBCursor](/apis/indexeddb/IDBCursor)[apis/indexeddb/IDBCursor](/apis/indexeddb/IDBCursor)

## Syntax

``` js
var  = .delete();
```

## Return Value

Returns an object of type
