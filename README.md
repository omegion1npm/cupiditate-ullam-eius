# @omegion1npm/cupiditate-ullam-eius <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

ES Proposal spec-compliant shim for Set.prototype.isSupersetOf. Invoke its "shim" method to shim `Set.prototype.isSupersetOf` if it is unavailable or noncompliant.

This package implements the [es-shim API](https://github.com/es-shims/api) interface. It works in an ES3-supported environment, and complies with the [proposed spec](https://github.com/tc39/proposal-set-methods). When shimmed, it uses [`es-set`](https://npmjs.com/es-set) to shim the `Set` implementation itself if needed.

Most common usage:
```js
var assert = require('assert');
var isSupersetOf = require('@omegion1npm/cupiditate-ullam-eius');

var set1 = new Set([1, 2]);
var set2 = new Set([2, 3]);
var set3 = new Set([1]);

assert.equal(isSupersetOf(set1, set2), false);
assert.equal(isSupersetOf(set2, set1), false);
assert.equal(isSupersetOf(set1, set3), true);

isSupersetOf.shim();

assert.equal(set1.isSupersetOf(set2), false);
assert.equal(set2.isSupersetOf(set1), false);
assert.equal(set1.isSupersetOf(set3), true);
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

## Set Method Packages
 - [union](https://npmjs.com/set.prototype.union)
 - [intersection](https://npmjs.com/set.prototype.intersection)
 - [difference](https://npmjs.com/set.prototype.difference)
 - [symmetricDifference](https://npmjs.com/set.prototype.symmetricdifference)
 - [isSubsetOf](https://npmjs.com/set.prototype.issubsetof)
 - [isSupersetOf](https://npmjs.com/@omegion1npm/cupiditate-ullam-eius)
 - [isDisjointFrom](https://npmjs.com/set.prototype.isdisjointfrom)

[package-url]: https://npmjs.com/package/@omegion1npm/cupiditate-ullam-eius
[npm-version-svg]: http://versionbadg.es/omegion1npm/cupiditate-ullam-eius.svg
[deps-svg]: https://david-dm.org/omegion1npm/cupiditate-ullam-eius.svg
[deps-url]: https://david-dm.org/omegion1npm/cupiditate-ullam-eius
[dev-deps-svg]: https://david-dm.org/omegion1npm/cupiditate-ullam-eius/dev-status.svg
[dev-deps-url]: https://david-dm.org/omegion1npm/cupiditate-ullam-eius#info=devDependencies
[testling-svg]: https://ci.testling.com/omegion1npm/cupiditate-ullam-eius.png
[testling-url]: https://ci.testling.com/omegion1npm/cupiditate-ullam-eius
[npm-badge-png]: https://nodei.co/npm/@omegion1npm/cupiditate-ullam-eius.png?downloads=true&stars=true
[license-image]: http://img.shields.io/npm/l/@omegion1npm/cupiditate-ullam-eius.svg
[license-url]: LICENSE
[downloads-image]: http://img.shields.io/npm/dm/@omegion1npm/cupiditate-ullam-eius.svg
[downloads-url]: http://npm-stat.com/charts.html?package=@omegion1npm/cupiditate-ullam-eius
[codecov-image]: https://codecov.io/gh/omegion1npm/cupiditate-ullam-eius/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/omegion1npm/cupiditate-ullam-eius/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/omegion1npm/cupiditate-ullam-eius
[actions-url]: https://github.com/omegion1npm/cupiditate-ullam-eius/actions
