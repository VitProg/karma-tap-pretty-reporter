# karma-tap-pretty-reporter

[![npm version](https://badge.fury.io/js/karma-tap-pretty-reporter.svg)](https://badge.fury.io/js/karma-tap-pretty-reporter)

> a Karma plugin to `report` and `prettify` TAP test results


## Installation

### npm
```bash
npm install karma karma-tap karma-tap-pretty-reporter --save-dev
```

### [optional] install a `prettify` package. See below supported prettifiers
```bash
npm install faucet --save-dev
```

## Usage

Add `karma.conf.js` file to project.

Example:
```js
// karma.conf.js
module.exports = function(config) {
  config.set({
    reporters: ['tap-pretty'],

    tapReporter: {
      prettifier: 'tap-spec',       // default 'standard TAP'
      separator: '****-----****'    // default 'false'
    },
  });
};
```

### Using `separator`
On Karma `autoWatch` mode you could need separate test run cycles. Set your own `separator` string or set to `true` for default separator. Current default separators, [prettifiers.js](https://github.com/bySabi/karma-tap-pretty-reporter/blob/master/src/prettifiers.js)

### Report to a file
Optionally you can save report to a file and turn off output to the console.

```js
// karma.conf.js

reporters: ['tap-pretty'],

tapReporter: {
  outputFile: './test.out.tap',
  disableStdout: true            // default 'false'
},

```

## Supported `prettifiers`
* [faucet](https://github.com/substack/faucet)
* [tap-spec](https://github.com/scottcorgan/tap-spec)
* [tap-min](https://github.com/gummesson/tap-min)
* [tap-diff](https://github.com/axross/tap-diff)
* [tap-notify](https://github.com/axross/tap-notify)
* [tap-summary](https://github.com/zoubin/tap-summary)
* [tap-markdown](https://github.com/Hypercubed/tap-markdown)


## Example usage
* [karma--tap--boilerplate](https://github.com/bySabi/karma--tap--boilerplate)


## Contributing
* Documentation improvement
* Feel free to send any PR

## License

[ISC][isc-license]

[isc-license]:./LICENSE
