
# [Quasar Extension Pack](https://marketplace.visualstudio.com/items?itemName=sskwrl.quasar-extension-pack)

[![quasar-logo](images/quasar-logo.png)](https://quasar.dev) | A [Quasar Framework](https://quasar.dev) development environment with useful VS Code extensions and minimal configuration. | [![quasar-logo](images/quasar-logo.png)](https://quasar.dev)
:-:|:-:|:-:

A list of included extensions can be seen in the Extension Pack tab.

## VS Code Settings file updates

### Standard ES-Lint rules

To edit the settings use the command `Open Settings JSON` in the Command Palette in the View menu (`ctrl+shift+p`).

```js
{
    "editor.formatOnPaste": true,
    "editor.formatOnSave": true,

    "eslint.autoFixOnSave": true,
    "eslint.validate": [
        {
            "language": "vue",
            "autoFix": true
        },
        {
            "language": "html",
            "autoFix": true"
        },
        {
            "language": "javascript",
            "autoFix": true
        }
    ],

    "javascript.format.insertSpaceBeforeFunctionParenthesis": true,
    "javascript.format.placeOpenBraceOnNewLineForControlBlocks": false,
    "javascript.format.placeOpenBraceOnNewLineForFunctions": false,

    "typescript.format.insertSpaceBeforeFunctionParenthesis": true,
    "typescript.format.placeOpenBraceOnNewLineForControlBlocks": false,
    "typescript.format.placeOpenBraceOnNewLineForFunctions": false,

    "vetur.format.defaultFormatter.html": "js-beautify-html",
    "vetur.format.defaultFormatter.js": "vscode-typescript"
}
```
### Prettier ES-Lint rules

To edit the settings use the command `Open Settings JSON` in the Command Palette in the View menu (`ctrl+shift+p`).

```js
{
    "editor.formatOnPaste": true,
    "editor.formatOnSave": true,

    "eslint.autoFixOnSave": true,
    "eslint.validate": [
        {
            "language": "vue",
            "autoFix": true
        },
        {
            "language": "html",
            "autoFix": true"
        },
        {
            "language": "javascript",
            "autoFix": true
        }
    ],

  "prettier.eslintIntegration":true,

  "vetur.format.defaultFormatter.html": "prettyhtml",
  "vetur.format.defaultFormatter.js": "prettier-eslint"
}
```
## Dubugger for Chrome

Please follow the instructions at [Debugger for Chrome](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-chrome)

Once you have a `.vscode/launch.json` file add or modify the configurations section to have the following contents.

<div style="background-color:grey;text-align:center;padding:5px;border-radius:15px";border:2px solid>Chrome must be started with `--remote-debugging-port=9222` for the attach configuration to work.</div>

```js
"configurations": [
    {
        "type": "chrome",
        "request": "attach",
        "name": "Attach to Chrome",
        "port": 9222,
        "webRoot": "${workspaceFolder}/src",
        "sourceMapPathOverrides": {
            "webpack:///./*": "${webRoot}/*",
            "webpack:///src/*": "${webRoot}/*",
            "webpack:///*": "*",
            "webpack:///./~/*": "${webRoot}/node_modules/*"
        }
    },
    {
        "type": "chrome",
        "request": "launch",
        "name": "Quasar Framework: chrome",
        "url": "http://localhost:8080/",
        "webRoot": "${workspaceFolder}/src",
        "sourceMapPathOverrides": {
            "webpack:///./*": "${webRoot}/*",
            "webpack:///src/*": "${webRoot}/*",
            "webpack:///*": "*",
            "webpack:///./~/*": "${webRoot}/node_modules/*"
        }
    }
]
```

## Enable and Optimize other extensions for use with Quasar Framework

To edit the settings use the command `Open Settings JSON` in the Command Palette in the View menu (`ctrl+shift+p`).

```js
{
  "attrsSorter.order": [
    "is",
    "v-for",
    "v-if",
    "v-else-if",
    "v-else",
    "v-show",
    "v-cloak",
    "v-once",
    "v-pre",
    "id",
    "ref",
    "key",
    "slot",
    "v-model",
    "v-model.+",
    "v-bind",
    "v-bind.+",
    ":.+",
    "v-text",
    "v-text.+",
    "v-html",
    "v-html.+",
    "class",
    "v-on.+",
    "@.+",
    "name",
    "data-.+",
    "ng-.+",
    "src",
    "for",
    "type",
    "href",
    "values",
    "title",
    "alt",
    "role",
    "aria-.+",
    "$unknown$"
  ],
  "workbench.iconTheme": "vscode-icons"
}
```

## Credits

- This is just a collection of extensions.  The real work was done by the authors of the included extensions thanks and contributions should be directed to them.

- Thanks to the people in [Quasar Discord](https://chat.quasar.dev) and [Quasar Forum](https://forum.quasar.dev) for suggestions and testing configuration values.