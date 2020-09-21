# util [![Build Status](https://travis-ci.org/defunctzombie/node-util.png?branch=master)](https://travis-ci.org/defunctzombie/node-util)

> Node.js's [util][util] module for all engines.

This implements the Node.js [`util`][util] module for environments that do not have it, like browsers.

## Install

### git

```shell
git clone https://iramiller.com/src/js/util/.git util
```

### npm

```shell
npm install @guld/util
```

## Usage

```javascript
import util from '../util/util.js')
import EventEmitter from '../events/events.js')

function MyClass() { EventEmitter.call(this) }
util.inherits(MyClass, EventEmitter)
```

## Browser Support

The `util` module uses ES6 features. Load it like any module with a static import `import 'util.js'`.

## API

See the [Node.js util docs][util].  `util` currently supports the Node 8 LTS API. However, some of the methods are outdated. The `inspect` and `format` methods included in this module are a lot more simple and barebones than the ones in Node.js.

## Contributing

PRs are very welcome! The main way to contribute to `util` is by porting features, bugfixes and tests from Node.js. Ideally, code contributions to this module are copy-pasted from Node.js and transpiled to ES5, rather than reimplemented from scratch. Matching the Node.js code as closely as possible makes maintenance simpler when new changes land in Node.js.
This module intends to provide exactly the same API as Node.js, so features that are not available in the core `util` module will not be accepted. Feature requests should instead be directed at [nodejs/node](https://github.com/nodejs/node) and will be added to this module once they are implemented in Node.js.

If there is a difference in behaviour between Node.js's `util` module and this module, please open an issue!

## License

[MIT](./LICENSE)

[util]: https://nodejs.org/docs/latest-v8.x/api/util.html
