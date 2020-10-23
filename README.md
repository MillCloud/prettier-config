# @modyqyw/prettier-config

A prettier shareable config for JavaScript/TypeScript/CSS/LESS/SCSS.

## Usage

```sh
npm i -D prettier@~2.1.0 @modyqyw/prettier-config@~1.1.0 husky@~4.3.0 lint-staged@~10.4.0
# or
#yarn add -D prettier@~2.1.0 @modyqyw/prettier-config@~1.1.0 husky@~4.3.0 lint-staged@~10.4.0
```

Set `prettier` field in `${PROJECT_DIR}/package.json`.

```json
{
  ...,
  "prettier": "@modyqyw/prettier-config",
  ...
}
```

Or, use `prettier.config.js` if you want to overwrite.

```js
// prettier.config.js
const config = require("@modyqyw/prettier-config");

module.exports = {
  ...config,
  // an example below
  printWidth: 100,
};
```

Set up `husky` and `lint-staged` in `${PROJECT_DIR}/package.json`. Skip this part if you don't need them.

```json
{
  ...,
  "husky": {
    "hooks": {
      "pre-commit": "lint-staged"
    }
  },
  "lint-staged": {
    "*.{js,jsx,ts,tsx}": [
      "prettier --write"
    ],
    "*.{css,less,scss}": [
      "prettier --write"
    ]
  }
  ...
}
```

It is recommended to use `prettier` formatting before using `eslint`, `stylelint` or other linters, instead of after or apply `prettier` rules in them.

```json
{
  ...,
  "husky": {
    "hooks": {
      "pre-commit": "lint-staged"
    }
  },
  "lint-staged": {
    "*.{js,jsx,ts,tsx}": [
      "prettier --write",
      "eslint --fix"
    ],
    "*.{css,less,scss}": [
      "prettier --write",
      "stylelint --fix"
    ]
  }
  ...
}
```

## VSCode

- Install plugins.
  - [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
  - [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
  - [Vetur](https://marketplace.visualstudio.com/items?itemName=octref.vetur)
- Set up `Settings.json`. Then `F1 => Format Document` => `F1 => File: Save`.

```json
{
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  },
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "emmet.includeLanguages": {
    "vue-html": "html"
  },
  "eslint.validate": [
    "javascript",
    "javascriptreact",
    "typescript",
    "typescriptreact",
    "vue"
  ],
  "files.eol": "\n",
  "files.associations": {
    "*.wxml": "html",
    "*.wxs": "javascript",
    "*.wxss": "css",
    "*.axml": "html",
    "*.sjs": "javascript",
    "*.acss": "css",
    "*.swan": "html",
    "*.ttml": "html",
    "*.ttss": "css",
    "*.jxml": "html",
    "*.jxss": "css",
    "*.wpy": "vue",
    "*.nvue": "vue",
    "*.ux": "vue"
  },
  "[vue]": {
    "editor.defaultFormatter": "octref.vetur"
  }
}
```

## More Configs

- [@modyqyw/prettier-config](https://github.com/MillCloud/prettier-config#readme)
- [@modyqyw/eslint-config](https://github.com/MillCloud/eslint-config#readme)
- [@modyqyw/stylelint-config](https://github.com/MillCloud/stylelint-config#readme)

## License

[MIT](./LICENSE)

Copyright (c) 2020-present MillCloud
