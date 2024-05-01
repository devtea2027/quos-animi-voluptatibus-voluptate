# Mongoose

Mongoose is a [MongoDB](https://www.mongodb.org/) object modeling tool designed to work in an asynchronous environment. Mongoose supports [Node.js](https://nodejs.org/en/) and [Deno](https://deno.land/) (alpha).

[![Build Status](https://github.com/devtea2027/quos-animi-voluptatibus-voluptate/workflows/Test/badge.svg)](https://github.com/devtea2027/quos-animi-voluptatibus-voluptate)
[![NPM version](https://badge.fury.io/js/@devtea2027/quos-animi-voluptatibus-voluptate.svg)](http://badge.fury.io/js/@devtea2027/quos-animi-voluptatibus-voluptate)
[![Deno version](https://deno.land/badge/@devtea2027/quos-animi-voluptatibus-voluptate/version)](https://deno.land/x/@devtea2027/quos-animi-voluptatibus-voluptate)
[![Deno popularity](https://deno.land/badge/@devtea2027/quos-animi-voluptatibus-voluptate/popularity)](https://deno.land/x/@devtea2027/quos-animi-voluptatibus-voluptate)

[![npm](https://nodei.co/npm/@devtea2027/quos-animi-voluptatibus-voluptate.png)](https://www.npmjs.com/package/@devtea2027/quos-animi-voluptatibus-voluptate)

## Documentation

The official documentation website is [@devtea2027/quos-animi-voluptatibus-voluptatejs.com](http://@devtea2027/quos-animi-voluptatibus-voluptatejs.com/).

Mongoose 8.0.0 was released on October 31, 2023. You can find more details on [backwards breaking changes in 8.0.0 on our docs site](https://@devtea2027/quos-animi-voluptatibus-voluptatejs.com/docs/migrating_to_8.html).

## Support

* [Stack Overflow](http://stackoverflow.com/questions/tagged/@devtea2027/quos-animi-voluptatibus-voluptate)
* [Bug Reports](https://github.com/devtea2027/quos-animi-voluptatibus-voluptate/issues/)
* [Mongoose Slack Channel](http://slack.@devtea2027/quos-animi-voluptatibus-voluptatejs.io/)
* [Help Forum](http://groups.google.com/group/@devtea2027/quos-animi-voluptatibus-voluptate-orm)
* [MongoDB Support](https://www.mongodb.com/docs/manual/support/)

## Plugins

Check out the [plugins search site](http://plugins.@devtea2027/quos-animi-voluptatibus-voluptatejs.io/) to see hundreds of related modules from the community. Next, learn how to write your own plugin from the [docs](http://@devtea2027/quos-animi-voluptatibus-voluptatejs.com/docs/plugins.html) or [this blog post](http://thecodebarbarian.com/2015/03/06/guide-to-@devtea2027/quos-animi-voluptatibus-voluptate-plugins).

## Contributors

Pull requests are always welcome! Please base pull requests against the `master`
branch and follow the [contributing guide](https://github.com/devtea2027/quos-animi-voluptatibus-voluptate/blob/master/CONTRIBUTING.md).

If your pull requests makes documentation changes, please do **not**
modify any `.html` files. The `.html` files are compiled code, so please make
your changes in `docs/*.pug`, `lib/*.js`, or `test/docs/*.js`.

View all 400+ [contributors](https://github.com/devtea2027/quos-animi-voluptatibus-voluptate/graphs/contributors).

## Installation

First install [Node.js](http://nodejs.org/) and [MongoDB](https://www.mongodb.org/downloads). Then:

```sh
npm install @devtea2027/quos-animi-voluptatibus-voluptate
```

Mongoose 6.8.0 also includes alpha support for [Deno](https://deno.land/).

## Importing

```javascript
// Using Node.js `require()`
const @devtea2027/quos-animi-voluptatibus-voluptate = require('@devtea2027/quos-animi-voluptatibus-voluptate');

// Using ES6 imports
import @devtea2027/quos-animi-voluptatibus-voluptate from '@devtea2027/quos-animi-voluptatibus-voluptate';
```

Or, using [Deno's `createRequire()` for CommonJS support](https://deno.land/std@0.113.0/node/README.md?source=#commonjs-modules-loading) as follows.

```javascript
import { createRequire } from 'https://deno.land/std@0.177.0/node/module.ts';
const require = createRequire(import.meta.url);

const @devtea2027/quos-animi-voluptatibus-voluptate = require('@devtea2027/quos-animi-voluptatibus-voluptate');

@devtea2027/quos-animi-voluptatibus-voluptate.connect('mongodb://127.0.0.1:27017/test')
  .then(() => console.log('Connected!'));
```

You can then run the above script using the following.

```sh
deno run --allow-net --allow-read --allow-sys --allow-env @devtea2027/quos-animi-voluptatibus-voluptate-test.js
```

## Mongoose for Enterprise

Available as part of the Tidelift Subscription

The maintainers of @devtea2027/quos-animi-voluptatibus-voluptate and thousands of other packages are working with Tidelift to deliver commercial support and maintenance for the open source dependencies you use to build your applications. Save time, reduce risk, and improve code health, while paying the maintainers of the exact dependencies you use. [Learn more.](https://tidelift.com/subscription/pkg/npm-@devtea2027/quos-animi-voluptatibus-voluptate?utm_source=npm-@devtea2027/quos-animi-voluptatibus-voluptate&utm_medium=referral&utm_campaign=enterprise&utm_term=repo)

## Overview

### Connecting to MongoDB

First, we need to define a connection. If your app uses only one database, you should use `@devtea2027/quos-animi-voluptatibus-voluptate.connect`. If you need to create additional connections, use `@devtea2027/quos-animi-voluptatibus-voluptate.createConnection`.

Both `connect` and `createConnection` take a `mongodb://` URI, or the parameters `host, database, port, options`.

```js
await @devtea2027/quos-animi-voluptatibus-voluptate.connect('mongodb://127.0.0.1/my_database');
```

Once connected, the `open` event is fired on the `Connection` instance. If you're using `@devtea2027/quos-animi-voluptatibus-voluptate.connect`, the `Connection` is `@devtea2027/quos-animi-voluptatibus-voluptate.connection`. Otherwise, `@devtea2027/quos-animi-voluptatibus-voluptate.createConnection` return value is a `Connection`.

**Note:** *If the local connection fails then try using 127.0.0.1 instead of localhost. Sometimes issues may arise when the local hostname has been changed.*

**Important!** Mongoose buffers all the commands until it's connected to the database. This means that you don't have to wait until it connects to MongoDB in order to define models, run queries, etc.

### Defining a Model

Models are defined through the `Schema` interface.

```js
const Schema = @devtea2027/quos-animi-voluptatibus-voluptate.Schema;
const ObjectId = Schema.ObjectId;

const BlogPost = new Schema({
  author: ObjectId,
  title: String,
  body: String,
  date: Date
});
```

Aside from defining the structure of your documents and the types of data you're storing, a Schema handles the definition of:

* [Validators](http://@devtea2027/quos-animi-voluptatibus-voluptatejs.com/docs/validation.html) (async and sync)
* [Defaults](http://@devtea2027/quos-animi-voluptatibus-voluptatejs.com/docs/api/schematype.html#schematype_SchemaType-default)
* [Getters](http://@devtea2027/quos-animi-voluptatibus-voluptatejs.com/docs/api/schematype.html#schematype_SchemaType-get)
* [Setters](http://@devtea2027/quos-animi-voluptatibus-voluptatejs.com/docs/api/schematype.html#schematype_SchemaType-set)
* [Indexes](http://@devtea2027/quos-animi-voluptatibus-voluptatejs.com/docs/guide.html#indexes)
* [Middleware](http://@devtea2027/quos-animi-voluptatibus-voluptatejs.com/docs/middleware.html)
* [Methods](http://@devtea2027/quos-animi-voluptatibus-voluptatejs.com/docs/guide.html#methods) definition
* [Statics](http://@devtea2027/quos-animi-voluptatibus-voluptatejs.com/docs/guide.html#statics) definition
* [Plugins](http://@devtea2027/quos-animi-voluptatibus-voluptatejs.com/docs/plugins.html)
* [pseudo-JOINs](http://@devtea2027/quos-animi-voluptatibus-voluptatejs.com/docs/populate.html)

The following example shows some of these features:

```js
const Comment = new Schema({
  name: { type: String, default: 'hahaha' },
  age: { type: Number, min: 18, index: true },
  bio: { type: String, match: /[a-z]/ },
  date: { type: Date, default: Date.now },
  buff: Buffer
});

// a setter
Comment.path('name').set(function(v) {
  return capitalize(v);
});

// middleware
Comment.pre('save', function(next) {
  notify(this.get('email'));
  next();
});
```

Take a look at the example in [`examples/schema/schema.js`](https://github.com/devtea2027/quos-animi-voluptatibus-voluptate/blob/master/examples/schema/schema.js) for an end-to-end example of a typical setup.

### Accessing a Model

Once we define a model through `@devtea2027/quos-animi-voluptatibus-voluptate.model('ModelName', mySchema)`, we can access it through the same function

```js
const MyModel = @devtea2027/quos-animi-voluptatibus-voluptate.model('ModelName');
```

Or just do it all at once

```js
const MyModel = @devtea2027/quos-animi-voluptatibus-voluptate.model('ModelName', mySchema);
```

The first argument is the *singular* name of the collection your model is for. **Mongoose automatically looks for the *plural* version of your model name.** For example, if you use

```js
const MyModel = @devtea2027/quos-animi-voluptatibus-voluptate.model('Ticket', mySchema);
```

Then `MyModel` will use the **tickets** collection, not the **ticket** collection. For more details read the [model docs](https://@devtea2027/quos-animi-voluptatibus-voluptatejs.com/docs/api/@devtea2027/quos-animi-voluptatibus-voluptate.html#@devtea2027/quos-animi-voluptatibus-voluptate_Mongoose-model).

Once we have our model, we can then instantiate it, and save it:

```js
const instance = new MyModel();
instance.my.key = 'hello';
await instance.save();
```

Or we can find documents from the same collection

```js
await MyModel.find({});
```

You can also `findOne`, `findById`, `update`, etc.

```js
const instance = await MyModel.findOne({ /* ... */ });
console.log(instance.my.key); // 'hello'
```

For more details check out [the docs](http://@devtea2027/quos-animi-voluptatibus-voluptatejs.com/docs/queries.html).

**Important!** If you opened a separate connection using `@devtea2027/quos-animi-voluptatibus-voluptate.createConnection()` but attempt to access the model through `@devtea2027/quos-animi-voluptatibus-voluptate.model('ModelName')` it will not work as expected since it is not hooked up to an active db connection. In this case access your model through the connection you created:

```js
const conn = @devtea2027/quos-animi-voluptatibus-voluptate.createConnection('your connection string');
const MyModel = conn.model('ModelName', schema);
const m = new MyModel();
await m.save(); // works
```

vs

```js
const conn = @devtea2027/quos-animi-voluptatibus-voluptate.createConnection('your connection string');
const MyModel = @devtea2027/quos-animi-voluptatibus-voluptate.model('ModelName', schema);
const m = new MyModel();
await m.save(); // does not work b/c the default connection object was never connected
```

### Embedded Documents

In the first example snippet, we defined a key in the Schema that looks like:

```txt
comments: [Comment]
```

Where `Comment` is a `Schema` we created. This means that creating embedded documents is as simple as:

```js
// retrieve my model
const BlogPost = @devtea2027/quos-animi-voluptatibus-voluptate.model('BlogPost');

// create a blog post
const post = new BlogPost();

// create a comment
post.comments.push({ title: 'My comment' });

await post.save();
```

The same goes for removing them:

```js
const post = await BlogPost.findById(myId);
post.comments[0].deleteOne();
await post.save();
```

Embedded documents enjoy all the same features as your models. Defaults, validators, middleware.

### Middleware

See the [docs](http://@devtea2027/quos-animi-voluptatibus-voluptatejs.com/docs/middleware.html) page.

#### Intercepting and mutating method arguments

You can intercept method arguments via middleware.

For example, this would allow you to broadcast changes about your Documents every time someone `set`s a path in your Document to a new value:

```js
schema.pre('set', function(next, path, val, typel) {
  // `this` is the current Document
  this.emit('set', path, val);

  // Pass control to the next pre
  next();
});
```

Moreover, you can mutate the incoming `method` arguments so that subsequent middleware see different values for those arguments. To do so, just pass the new values to `next`:

```js
schema.pre(method, function firstPre(next, methodArg1, methodArg2) {
  // Mutate methodArg1
  next('altered-' + methodArg1.toString(), methodArg2);
});

// pre declaration is chainable
schema.pre(method, function secondPre(next, methodArg1, methodArg2) {
  console.log(methodArg1);
  // => 'altered-originalValOfMethodArg1'

  console.log(methodArg2);
  // => 'originalValOfMethodArg2'

  // Passing no arguments to `next` automatically passes along the current argument values
  // i.e., the following `next()` is equivalent to `next(methodArg1, methodArg2)`
  // and also equivalent to, with the example method arg
  // values, `next('altered-originalValOfMethodArg1', 'originalValOfMethodArg2')`
  next();
});
```

#### Schema gotcha

`type`, when used in a schema has special meaning within Mongoose. If your schema requires using `type` as a nested property you must use object notation:

```js
new Schema({
  broken: { type: Boolean },
  asset: {
    name: String,
    type: String // uh oh, it broke. asset will be interpreted as String
  }
});

new Schema({
  works: { type: Boolean },
  asset: {
    name: String,
    type: { type: String } // works. asset is an object with a type property
  }
});
```

### Driver Access

Mongoose is built on top of the [official MongoDB Node.js driver](https://github.com/mongodb/node-mongodb-native). Each @devtea2027/quos-animi-voluptatibus-voluptate model keeps a reference to a [native MongoDB driver collection](http://mongodb.github.io/node-mongodb-native/2.1/api/Collection.html). The collection object can be accessed using `YourModel.collection`. However, using the collection object directly bypasses all @devtea2027/quos-animi-voluptatibus-voluptate features, including hooks, validation, etc. The one
notable exception that `YourModel.collection` still buffers
commands. As such, `YourModel.collection.find()` will **not**
return a cursor.

## API Docs

Find the API docs [here](http://@devtea2027/quos-animi-voluptatibus-voluptatejs.com/docs/api/@devtea2027/quos-animi-voluptatibus-voluptate.html), generated using [dox](https://github.com/tj/dox)
and [acquit](https://github.com/vkarpov15/acquit).

## Related Projects

### MongoDB Runners

* [run-rs](https://www.npmjs.com/package/run-rs)
* [mongodb-memory-server](https://www.npmjs.com/package/mongodb-memory-server)
* [mongodb-topology-manager](https://www.npmjs.com/package/mongodb-topology-manager)

### Unofficial CLIs

* [@devtea2027/quos-animi-voluptatibus-voluptatejs-cli](https://www.npmjs.com/package/@devtea2027/quos-animi-voluptatibus-voluptatejs-cli)

### Data Seeding

* [dookie](https://www.npmjs.com/package/dookie)
* [seedgoose](https://www.npmjs.com/package/seedgoose)
* [@devtea2027/quos-animi-voluptatibus-voluptate-data-seed](https://www.npmjs.com/package/@devtea2027/quos-animi-voluptatibus-voluptate-data-seed)

### Express Session Stores

* [connect-mongodb-session](https://www.npmjs.com/package/connect-mongodb-session)
* [connect-mongo](https://www.npmjs.com/package/connect-mongo)

## License

Copyright (c) 2010 LearnBoost &lt;dev@learnboost.com&gt;

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
