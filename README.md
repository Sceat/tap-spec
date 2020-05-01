> Forked from [tap-spec](https://github.com/scottcorgan/tap-spec)

# tap-spec (Emoji patch) [![NPM version](https://img.shields.io/npm/v/tap-spec-emoji.svg?style=flat-square)](https://www.npmjs.com/package/tap-spec-emoji) [![NPM download count](https://img.shields.io/npm/dm/tap-spec-emoji.svg?style=flat-square)](https://www.npmjs.com/package/tap-spec-emoji)

Formatted TAP output like Mocha's spec reporter

<p align=center>
  <img width=600 src="https://i.imgur.com/CDiF3bE.png" />
</p>

## Patch Motivation

Using a terminal with emoji support, the tests output become pretty ugly. This package use different emojis instead.
You may still use the original lib for your CI in case it doesn't support emojis (because it support char fallbacks), but on your local computer this version allow for a better output

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
