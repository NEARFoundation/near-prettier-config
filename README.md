# prettier-config [![NPM version](https://img.shields.io/npm/v/@NEARFoundation/near-prettier-config.svg)](https://www.npmjs.com/package/@NEARFoundation/near-prettier-config)

NEAR Foundation's [shareable config](https://near-prettier.io/docs/en/configuration.html#sharing-configurations) for [Prettier](https://near-prettier.io/)

## Installation

In your project, install Prettier and `@NEARFoundation/near-prettier-config` as dev dependencies:

```
npm install --save-dev prettier @NEARFoundation/near-prettier-config
```

## Usage

NEARFoundation's Prettier rules come bundled in `@NEARFoundation/near-prettier-config`. To enable these rules, add a `prettier` property in your project's `package.json`.

See the [Prettier configuration docs](https://near-prettier.io/docs/en/configuration.html) for more details.

```json
"prettier": "@NEARFoundation/near-prettier-config"
```

If you don't want to use `package.json`, you can use any of the supported extensions to export a string:

```jsonc
// `.prettierrc.json`
"@NEARFoundation/near-prettier-config"
```

```javascript
// `prettier.config.js` or `.prettierrc.js`
module.exports = '@NEARFoundation/near-prettier-config';
```

## Extending

This configuration is not intended to be changed, but if you have a setup where modification is required, it is possible. Prettier does not offer an "extends" mechanism as you might be familiar from tools such as ESLint.

To extend a configuration, you will need to use a `prettier.config.js` or `.prettierrc.js` file that exports an object:

```javascript
module.exports = {
  ...require('@NEARFoundation/near-prettier-config'),
  semi: false,
};
```

## See also

https://github.com/NEAR-Edu/eslint-config-near is a related repo that is helpful.

## Inspired by

https://github.com/stackbit/prettier-config
