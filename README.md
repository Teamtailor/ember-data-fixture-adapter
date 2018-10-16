# Ember Data Fixture Adapter

[![Build Status](https://travis-ci.org/emberjs/ember-data-fixture-adapter.svg)](https://travis-ci.org/emberjs/ember-data-fixture-adapter)

This addon contains the FixtureAdapter from Ember Data. The
FixtureAdapter lets you find, store, modify, and delete records using an
in-memory store.

The FixtureAdapter was removed from Ember Data core in May 2015 due to
the lack of an interested maintainer and overall bugginess. We recommend
you switch to using an AJAX stubbing library like
[Pretender](https://github.com/trek/pretender).

**This addon is currently not maintained by the Ember Data team.**
However, we will be happy to merge documentation fixes.

Installation
------------------------------------------------------------------------------

You can use it as an addon using `ember install ember-data-fixture-adapter`.

If you are using it in globals mode, you can use [Ember
Giftwrap](https://github.com/ef4/ember-giftwrap) to build it for your
application.

## Usage

You can define a `FIXTURES` array on your model with some data you would
like available by default:

```javascript
import DS from 'ember-data';

var Post = DS.Model.extend({
  title: DS.attr()
});

Post.reopenClass({
  FIXTURES: [
    {
      id: 1,
      title: "Something something Basecamp"
    }
  ]
});

export default Post;
```

Then, in your tests, set your app's application adapter to the
FixtureAdapter:

```javascript
// app/adapters/application.js
export { default } from 'ember-data-fixture-adapter';
```

## Development Installation

* `git clone` this repository
* `npm install`

### Linting

* `npm run lint:hbs`
* `npm run lint:js`
* `npm run lint:js -- --fix`

### Running tests

* `ember test` – Runs the test suite on the current Ember version
* `ember test --server` – Runs the test suite in "watch mode"
* `ember try:each` – Runs the test suite against multiple Ember versions

### Running the dummy application

* `ember test`
* `ember test --server`

For more information on using ember-cli, visit [https://ember-cli.com/](https://ember-cli.com/).

License
------------------------------------------------------------------------------

This project is licensed under the [MIT License](LICENSE.md).
