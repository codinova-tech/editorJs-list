![](https://badgen.net/badge/Editor.js/v2.0/blue)

# List Tool for Editor.js

This Tool for the [Editor.js](https://editorjs.io) allows you to add ordered or unordered (bulleted) lists to your article.

![ezgif com-video-to-gif](https://user-images.githubusercontent.com/55910733/89700109-3b5cd100-d949-11ea-9e54-8153fe6c7465.gif)

## Installation

### Install via NPM

Get the package

```shell
npm i --save @editorjs/list
```
```shell
yarn add @editorjs/list
```

Include module at your application

```javascript
import List from '@editorjs/list';
```

### Download to your project's source dir

1. Upload folder `dist` from repository
2. Add `dist/bundle.js` file to your page.

### Load from CDN

Load the script from [jsDelivr CDN](https://www.jsdelivr.com/package/npm/@editorjs/list) and connect to your page.

```html
<script src="https://cdn.jsdelivr.net/npm/@editorjs/list@latest"></script>
```

## Usage

Add the List Tool to the `tools` property of the Editor.js initial config.

```javascript
import EditorJS from '@editorjs/editorjs';
import List from '@editorjs/list';

var editor = EditorJS({
  // ...
  tools: {
    ...
    list: {
      class: List,
      inlineToolbar: true,
    },
  },
});
```

## Config Params

This Tool has no config params

## Tool's settings

![](https://capella.pics/bf5a42e4-1350-499d-a728-493b0fcaeda4.jpg)

You can choose list`s type.

## Output data

| Field | Type       | Description                            |
| ----- | ---------- | -------------------------------------- |
| style | `string`   | type of a list: `ordered` or `unordered` |
| items | `string[]` | the array of list's items              |


```json
{
    "type" : "list",
    "data" : {
        "style" : "unordered",
        "items" : [
            "It is a block-styled editor",
            [
                "It returns clean data output in JSON",
                [
                    "Here comes the sub lists",
                    "with both ordered and unordered",
                    [
                        "Just press tab and sub list will be created<br>"
                    ]
                ]
            ],
            "Designed to be extendable and pluggable with a simple API"
        ]
    }
},
```

## I18n support

This tool supports the [i18n api](https://editorjs.io/i18n-api).
To localize UI labels, put this object to your i18n dictionary under the `tools` section:

```json
"list": {
  "Ordered": "Нумерованный",
  "Unordered": "Маркированный"
}
```

See more instructions about Editor.js internationalization here: [https://editorjs.io/internationalization](https://editorjs.io/internationalization)
