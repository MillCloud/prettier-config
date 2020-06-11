# @modyqyw/prettier-config

A prettier shareable config.

## Usage

- Install the config.

```sh
npm i prettier@~2.0.0 @modyqyw/prettier-config@~1.0.0 -D
```

For yarn, run scripts below.

```sh
yarn add prettier@~2.0.0 @modyqyw/prettier-config@~1.0.0 -D
```

- Set up.

```jsonc
// package.json
{
  ...,
  "prettier": "@modyqyw/prettier-config",
  ...
}
```

If you want overwrite, use `prettier.config.js`.

```js
// prettier.config.js
module.exports = {
  ...require("@modyqyw/prettier-config"),
  printWidth: 120,
};
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
    "source.fixAll": true
  },
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "emmet.includeLanguages": {
    "javascript": "javascriptreact",
    "typescript": "typescriptreact",
    "json": "jsonc"
  },
  "eslint.validate": [
    "javascript",
    "javascriptreact",
    "typescript",
    "typescriptreact",
    "html",
    "vue",
    "vue-html"
  ],
  "files.eol": "\n",
  "files.associations": {
    "*.js": "javascriptreact",
    "*.ts": "typescriptreact",
    "*.wxml": "html",
    "*.wxs": "javascriptreact",
    "*.wxss": "css",
    "*.axml": "html",
    "*.sjs": "javascriptreact",
    "*.acss": "css",
    "*.wpy": "html",
    "*.json": "jsonc",
    "*.nvue": "vue",
    "*.ux": "vue"
  },
  "[vue]": {
    "editor.defaultFormatter": "octref.vetur"
  }
}
```

## License

[MIT](./LICENSE)

Copyright (c) 2020-present Millcloud
