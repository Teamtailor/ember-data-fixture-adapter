## Module Report
### Unknown Global

**Global**: `Ember.Registry`

**Location**: `tests/test-helper.js` at line 15

```js
  options = options || {};

  var registry = env.registry = new Ember.Registry();
  var container = env.container = registry.container();

```

### Unknown Global

**Global**: `Ember.Logger`

**Location**: `tests/test-helper.js` at line 59

```js
    // handle the error.
    if (reason && reason instanceof Error) {
      Ember.Logger.log(reason, reason.stack);
      throw reason;
    }
```

### Unknown Global

**Global**: `Ember.EnumerableUtils`

**Location**: `addon/index.js` at line 7

```js
var indexOf = Array.prototype.indexOf && function(array, item) {
  return array.indexOf(item);
} || Ember.EnumerableUtils.indexOf;

var map = Array.prototype.map && function(array, cb, binding) {
```

### Unknown Global

**Global**: `Ember.EnumerableUtils`

**Location**: `addon/index.js` at line 11

```js
var map = Array.prototype.map && function(array, cb, binding) {
  return array.map(cb, binding);
} || Ember.EnumerableUtils.map;

var counter = 0;
```

### Unknown Global

**Global**: `Ember.testing`

**Location**: `tests/unit/fixture-adapter-test.js` at line 37

```js

    // Enable setTimeout.
    Ember.testing = false;

    Person.FIXTURES = [];
```

### Unknown Global

**Global**: `Ember.testing`

**Location**: `tests/unit/fixture-adapter-test.js` at line 43

```js
  },
  teardown: function() {
    Ember.testing = true;

    run(env.container, 'destroy');
```
