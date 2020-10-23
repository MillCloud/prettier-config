# @modyqyw/prettier-config

A prettier shareable config for JavaScript/TypeScript/CSS/LESS/SCSS.

## Usage

```sh
npm i -D prettier@~2.1.0 @modyqyw/prettier-config@~1.1.0
# or
#yarn add -D prettier@~2.1.0 @modyqyw/prettier-config@~1.1.0
```

Set `prettier` field in `${PROJECT_DIR}/package.json`.

```json
{
  ...,
  "prettier": "@modyqyw/prettier-config",
  ...
}
```

Or, use `${PROJECT_DIR}/prettier.config.js` if you want to overwrite.

```js
// ${PROJECT_DIR}/prettier.config.js
const config = require("@modyqyw/prettier-config");

module.exports = {
  ...config,
  // an example below
  printWidth: 100,
};
```

## VSCode

- Install plugins.
  - [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
  - [Vetur](https://marketplace.visualstudio.com/items?itemName=octref.vetur)
- Set up `Settings.json`. Then `F1 => Format Document` => `F1 => File: Save`.

```json
{
  "editor.defaultFormatter": "esbenp.prettier-vscode",
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

For auto formatting, use `"editor.formatOnSave": true`.

## More Configs

- [@modyqyw/prettier-config](https://github.com/MillCloud/prettier-config#readme)
- [@modyqyw/eslint-config](https://github.com/MillCloud/eslint-config#readme)
- [@modyqyw/stylelint-config](https://github.com/MillCloud/stylelint-config#readme)

## License

[MIT](./LICENSE)

Copyright (c) 2020-present MillCloud
