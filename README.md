# endpoints-model [![Build Status](https://secure.travis-ci.org/endpoints/model.png)](http://travis-ci.org/endpoints/model)
> model layer for the endpoints framework

[![NPM](https://nodei.co/npm/endpoints-model.png)](https://nodei.co/npm/endpoints-model/)

a quick and dirty extraction of some tools i use all the time for building rest apis.

## Example
```js
const Model = require('endpoints-model');
const Knex = require('knex')({
  client: "pg",
  connection: {
    host: "localhost",
    user: "user",
    database: "db",
    password: "pass"
  },
});
const Bookshelf = 
const BaseModel = Model({
  Bookshelf: require('bookshelf')(Knex),
  Validator: require('checkit'),
  linkPrefix: '/api/v1' // when a model is serialized, the automatically generated `links` key may need a prefix to produce the correct endpoint URL.
});
```
