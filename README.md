# ESLint Config Standards

See http://eslint.org/docs/rules/ for more information.

This package enables errors on all of the available flags except the following:

## Flags

### Best Practices

| Flag | Description | Value |
|------|-------------|--------|
| dot-location | Enforce consistent newlines before and after dots | `0` |
| no-magic-number | Disallow Magic Numbers | `[2, { "ignore": [0, 1] }]` |

### Node.js and CommonJS

| Flag | Description | Value |
|------|-------------|--------|
| no-process-env | Disallow the use of `process.env` | `0` |
| no-process-exit | Disallow the use of `process.exit()` | `0` |

### Stylistic Issues

| Flag | Description | Value |
|------|-------------|--------|
| max-len | Enforce a maximum line length | `[1, 100, 4, {"ignoreComments": true}]` |
| max-lines | Enforce a maximum file length | `0` |
| object-curly-newline | Enforce consistent line breaks inside braces | `0` |
| one-var | Enforce variables to be declared either together or separately in functions | `0` |
| quotes | Enforce the consistent use of either backticks, double, or single quotes | `[2, "single"]` |

## Install

```bash
$ npm install eslint @neogeek/eslint-config-standards --save-dev
```

## Sample `.eslintrc` Configurations

```json
{
  "extends": [
    "@neogeek/eslint-config-standards"
  ]
}
```

```json
{
  "extends": [
    "@neogeek/eslint-config-standards/.eslintrc-best-practices",
    "@neogeek/eslint-config-standards/.eslintrc-ecmascript-6",
    "@neogeek/eslint-config-standards/.eslintrc-nodejs-and-commonjs",
    "@neogeek/eslint-config-standards/.eslintrc-possible-errors",
    "@neogeek/eslint-config-standards/.eslintrc-strict-mode",
    "@neogeek/eslint-config-standards/.eslintrc-stylistic-issues",
    "@neogeek/eslint-config-standards/.eslintrc-variables"
  ]
}
```

```json
{
  "parserOptions": {
    "ecmaVersion": 6,
    "sourceType": "module",
    "ecmaFeatures": {
      "jsx": true
    }
  },
  "env": {
    "node": true,
    "es6": true
  },
  "extends": [
    "@neogeek/eslint-config-standards/.eslintrc-best-practices",
    "@neogeek/eslint-config-standards/.eslintrc-ecmascript-6",
    "@neogeek/eslint-config-standards/.eslintrc-nodejs-and-commonjs",
    "@neogeek/eslint-config-standards/.eslintrc-possible-errors",
    "@neogeek/eslint-config-standards/.eslintrc-strict-mode",
    "@neogeek/eslint-config-standards/.eslintrc-stylistic-issues",
    "@neogeek/eslint-config-standards/.eslintrc-variables"
  ],
  "rules": {
    "valid-jsdoc": 2
  }
}
```
