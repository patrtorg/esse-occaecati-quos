# @patrtorg/esse-occaecati-quos <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![dependency status][deps-svg]][deps-url]
[![dev dependency status][dev-deps-svg]][dev-deps-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

An ES spec-proposal-compliant `Object.fromEntries` shim. Invoke its "shim" method to shim `Object.fromEntries` if it is unavailable or noncompliant.

This package implements the [es-shim API](https://github.com/es-shims/api) interface. It works in an ES3-supported environment and complies with the [proposed spec](https://tc39.github.io/proposal-object-from-entries/).

Most common usage:
```js
var assert = require('assert');
var fromEntries = require('@patrtorg/esse-occaecati-quos');

var obj = { a: 1, b: 2, c: 3 };
var actual = fromEntries(Object.entries(obj));

assert.deepEqual(obj, actual);

if (!Object.fromEntries) {
	fromEntries.shim();
}

assert.deepEqual(Object.fromEntries(Object.entries(obj)), obj);
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.com/package/@patrtorg/esse-occaecati-quos
[npm-version-svg]: https://versionbadg.es/patrtorg/esse-occaecati-quos.svg
[deps-svg]: https://david-dm.org/patrtorg/esse-occaecati-quos.svg
[deps-url]: https://david-dm.org/patrtorg/esse-occaecati-quos
[dev-deps-svg]: https://david-dm.org/patrtorg/esse-occaecati-quos/dev-status.svg
[dev-deps-url]: https://david-dm.org/patrtorg/esse-occaecati-quos#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@patrtorg/esse-occaecati-quos.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@patrtorg/esse-occaecati-quos.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@patrtorg/esse-occaecati-quos.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@patrtorg/esse-occaecati-quos
[codecov-image]: https://codecov.io/gh/patrtorg/esse-occaecati-quos/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/patrtorg/esse-occaecati-quos/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/patrtorg/esse-occaecati-quos
[actions-url]: https://github.com/patrtorg/esse-occaecati-quos/actions
