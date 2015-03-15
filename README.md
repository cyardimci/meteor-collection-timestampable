[![Gitter](https://img.shields.io/badge/gitter-join_chat-brightgreen.svg)]
(https://gitter.im/zimme/meteor-collection-timestampable)
[![Code Climate](http://img.shields.io/codeclimate/github/zimme/meteor-collection-timestampable.svg)]
(https://codeclimate.com/github/zimme/meteor-collection-timestampable)

# Timestamps for collections

Add timestamps to collections

This package uses `aldeed:simple-schema`, `aldeed:collection2` and `aldeed:autoform`
if they are available in the project.

### Install
```sh
meteor add zimme:collection-timestampable
```

### Usage

```js
Posts = new Mongo.Collection('posts');

// Default options
Posts.attachBehaviour('timestampable');

// Custom options
Posts.attachBehaviour('timestampable', {
  createdAt: 'insertedAt'
  createdBy: 'insertedBy'
  updatedAt: 'modifiedAt'
  updatedBy: false
});
```

### Options

Available options are:

`createdAt`, `createdBy`, `updatedAt`, `updatedBy`

Valid values are:

`'string'` will be used as field name.  
`false` field will be omitted.
