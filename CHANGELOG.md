### v1.0.0: November 29, 2015
 * [Tests] up to `node` `v5.1`
 * [Tests] fix npm upgrades on older nodes
 * [Dev Deps] update `uglify-js`, `docco`, `should`, `mocha`, and fix test pollution

### v0.4.5: November 29, 2015
 * [Fix] Ensure that dollar signs are properly escaped in substitutions (#43)
 * [Docs] use SPDX-compliant license string (#44)

### v0.4.4: October 26, 2015
 * [New] Add `unset` method (#43)
 * [Tests] test on travis-ci

### v0.4.3: June 26, 2015
 * Add `.has(key)` method (thanks @scarfacedeb).
 * Add UMD wrapper for AMD support (thanks @TomOne).

### v0.4.2: March 13, 2015
 * Allow blank translations.

### v0.4.1: July 14, 2014
 * Added support for `warn` option for custom error handler (thanks @terinjokes).
 * Added some more plural forms (thanks @jgill333).

### v0.4.0: May 22, 2014
 * Added support for nested phrase objects to `extend()` and in the `phrases` option in the constructor.

### v0.3.0: August 6, 2013
 * _Breaking change_: Removed `pluralize()` method; instead, just use the `t()` method, passing in a `smart_count` option.
 * _Breaking change_: Removed the ability to use `Array`, `Backbone.Collection`, etc. instances for the `smart_count` option; instead, must pass a `Number`.
 * Allow passing `Number` as second argument to `t()`, which gets converted to the options object `{smart_count: <my number>}`.

### v0.2.1: May 2, 2013
 * Added `allowMissing` option to let the phrase key be the default translation (thanks @ziad-saab).

### v0.2.0: Dec 20, 2012
 * _Breaking change_: Moved from Singleton pattern to class-based. Now you create an instance of the `Polyglot` class rather than using class methods directly on it. The reason is to allow maintaining multiple sets of phrases, which is something we ran into at Airbnb with a highly-concurrent Express app.
 * _Breaking change_: Removed the built-in Handlebars helpers, because Handlebars is a singleton, and it's messy to create a single helper function that can be bound to different Polyglot instances.  Instead, it's super easy to create your own, based on your requirements.
