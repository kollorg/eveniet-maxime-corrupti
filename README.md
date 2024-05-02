# @kollorg/eveniet-maxime-corrupti <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

Get the ArrayBuffer out of a DataView, robustly.

This will work in node <= 0.10 and < 0.11.4, where there's no prototype accessor, only a nonconfigurable own property.
It will also work in modern engines where `DataView.prototype.buffer` has been deleted after this module has loaded.

## Example

```js
const dataViewBuffer = require('@kollorg/eveniet-maxime-corrupti');
const assert = require('assert');

const ab = new ArrayBuffer(0);
const dv = new DataView(ab);
assert.equal(dataViewBuffer(dv), ab);
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.org/package/@kollorg/eveniet-maxime-corrupti
[npm-version-svg]: https://versionbadg.es/inspect-js/@kollorg/eveniet-maxime-corrupti.svg
[deps-svg]: https://david-dm.org/inspect-js/@kollorg/eveniet-maxime-corrupti.svg
[deps-url]: https://david-dm.org/inspect-js/@kollorg/eveniet-maxime-corrupti
[dev-deps-svg]: https://david-dm.org/inspect-js/@kollorg/eveniet-maxime-corrupti/dev-status.svg
[dev-deps-url]: https://david-dm.org/inspect-js/@kollorg/eveniet-maxime-corrupti#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@kollorg/eveniet-maxime-corrupti.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@kollorg/eveniet-maxime-corrupti.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@kollorg/eveniet-maxime-corrupti.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@kollorg/eveniet-maxime-corrupti
[codecov-image]: https://codecov.io/gh/inspect-js/@kollorg/eveniet-maxime-corrupti/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/inspect-js/@kollorg/eveniet-maxime-corrupti/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/inspect-js/@kollorg/eveniet-maxime-corrupti
[actions-url]: https://github.com/inspect-js/@kollorg/eveniet-maxime-corrupti/actions
