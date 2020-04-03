## Motivation

Using a terminal with emoji support, the tests output become pretty ugly. This package use different emojis instead.

### Original

![](https://i.imgur.com/yNCoue7.png)

### Patched

![](https://i.imgur.com/CDiF3bE.png)

> Forked from [tap-spec](https://github.com/scottcorgan/tap-spec)

# tap-spec (Emoji patch) [![NPM version](https://img.shields.io/npm/v/tap-spec-emoji.svg?style=flat-square)](https://www.npmjs.com/package/tap-spec-emoji) [![NPM download count](https://img.shields.io/npm/dm/tap-spec-emoji.svg?style=flat-square)](https://www.npmjs.com/package/tap-spec-emoji)

Formatted TAP output like Mocha's spec reporter

![iterm - 2 bash - may 29 2015 at 10 17 am screen shot](https://cloud.githubusercontent.com/assets/974723/7888261/03366236-05ec-11e5-9f94-d9c2707526b7.png)

## Install

```
npm install tap-spec-emoji --save-dev
```

## Usage

### Streaming

```js
var test = require('tape');
var tapSpec = require('tap-spec-emoji');

test.createStream()
  .pipe(tapSpec())
  .pipe(process.stdout);
```

### CLI

**package.json**

```json
{
  "name": "module-name",
  "scripts": {
    "test": "node ./test/tap-test.js | tap-spec-emoji"
  }
}
```

Then run with `npm test`

**Terminal**

```
tape test/index.js | node_modules/.bin/tap-spec-emoji
```

**Testling**

```
npm install testling -g
testling test/index.js | node_modules/.bin/tap-spec-emoji
```
