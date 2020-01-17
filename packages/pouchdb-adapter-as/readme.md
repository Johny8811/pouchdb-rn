pouchdb-adapter-as
======

PouchDB adapter using **community/asyncStorage** as its data store. Its adapter name is `'asyncstorage'`.

[![npm Package](https://img.shields.io/npm/v/pouchdb-adapter-asyncstorage.svg)](https://www.npmjs.com/package/pouchdb-adapter-as) [![travis-ci.org](https://travis-ci.org/stockulus/pouchdb-react-native.svg)](https://travis-ci.org/stockulus/pouchdb-react-native) [![js-standard-style](https://img.shields.io/badge/code%20style-standard-brightgreen.svg)](http://standardjs.com/) [![license](https://img.shields.io/npm/l/pouchdb-adapter-asyncstorage.svg?maxAge=2592000)](https://opensource.org/licenses/MIT)

### Usage

```bash
npm install pouchdb-adapter-as --save
```

```js
import PouchDB from 'pouchdb-core'
PouchDB.plugin(require('pouchdb-adapter-as').default)
const db = new PouchDB('mydb', {adapter: 'asyncstorage'})

// use PouchDB
db.get('4711')
  .then(doc => console.log(doc))

```

### Android limit

On Android asyncstorage has a limitation of 6 MB per default, you might want to increase it

```java
// MainApplication.getPackages()
long size = 50L * 1024L * 1024L; // 50 MB
com.facebook.react.modules.storage.ReactDatabaseSupplier.getInstance(getApplicationContext()).setMaximumSize(size);
```

For full API documentation and guides on PouchDB, see [PouchDB.com](http://pouchdb.com/). For details on PouchDB sub-packages, see the [Custom Builds documentation](http://pouchdb.com/custom.html).

---
[![GitHub stars](https://img.shields.io/github/stars/stockulus/pouchdb-react-native.svg?style=social&label=Star)](https://github.com/stockulus/pouchdb-rn)
