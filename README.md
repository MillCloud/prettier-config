# @modyqyw/prettier-config

A prettier shareable config for JavaScript/TypeScript/CSS/LESS/SCSS.

Will be dropped in the future. Try [@modyqyw/fabric](#more-configs).

[Github](https://github.com/MillCloud/prettier-config#readme) | [Gitee](https://gitee.com/millcloud/prettier-config#readme)

## Usage

```sh
npm i -D prettier@~2.1.2 @modyqyw/prettier-config@~1.1.8
# or
#yarn add -D prettier@~2.1.2 @modyqyw/prettier-config@~1.1.8
```

Set `prettier` field in `${PROJECT_DIR}/package.json`.

```json
{
  ...,
  "prettier": "@modyqyw/prettier-config",
  ...
}
```

Or use `${PROJECT_DIR}/prettier.config.js` if you want to overwrite.

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

- `@modyqyw/prettier-config` - [Github](https://github.com/MillCloud/prettier-config#readme) [Gitee](https://gitee.com/millcloud/prettier-config#readme)
- `@modyqyw/eslint-config` - [Github](https://github.com/MillCloud/eslint-config#readme) [Gitee](https://gitee.com/millcloud/eslint-config#readme)
- `@modyqyw/stylelint-config` - [Github](https://github.com/MillCloud/stylelint-config#readme) [Gitee](https://gitee.com/millcloud/stylelint-config#readme)

`@modyqyw/eslint-config` and `@modyqyw/stylelint-config` do not use any `Prettier` config and plugin, while `@modyqyw/fabric` does.

## License

[MIT](./LICENSE)

Copyright (c) 2020-present MillCloud
