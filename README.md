![](https://badgen.net/badge/Editor.js/v2.0/blue)

# Header Tool

Provides Headings Blocks for the [Editor.js](https://ifmo.su/editor).

## Installation

### Install via NPM

Get the package

```shell
npm i --save-dev @editorjs/header
```

Include module at your application

```javascript
const Header = require('@editorjs/header');
```

### Download to your project's source dir

1. Upload folder `dist` from repository
2. Add `dist/bundle.js` file to your page.

### Load from CDN
You can load specific version of package from [jsDelivr CDN](https://www.jsdelivr.com/package/npm/@editorjs/header).

`https://cdn.jsdelivr.net/npm/@editorjs/header@2.0.4`

Then require this script on page with Editor.js.

```html
<script src="..."></script>
```

## Usage

Add a new Tool to the `tools` property of the Editor.js initial config.

```javascript
var editor = EditorJS({
  ...
  
  tools: {
    ...
    header: Header,
  },
  
  ...
});
```

## Shortcut

You can insert this Block by a useful shortcut. Set it up with the `tools[].shortcut` property of the Editor's initial config.

```javascript
var editor = EditorJS({
  ...
  
  tools: {
    ...
    header: {
      class: Header,
      shortcut: 'CMD+SHIFT+H',
    },
  },
  
  ...
});
```

## Config Params

| Field       | Type     | Description                 |
| ----------- | -------- | --------------------------- |
| placeholder | `string` | header's placeholder string |

```javascript
var editor = EditorJS({
  ...
  
  tools: {
    ...
    header: {
      class: Header,
      config: {
        placeholder: 'Enter a header'
      }
    }
  }
  
  ...
});
```

## Tool's settings

![](https://capella.pics/5ef43c5b-441f-48bd-9b53-854f57f8161b.jpg)

You can select one of three levels for heading.

## Output data

| Field  | Type     | Description                                   |
| ------ | -------- | --------------------------------------------- |
| text   | `string` | header's text                                 |
| level  | `number` | level of header: 2 for H2, 3 for H3, 4 for H4 |


```json
{
    "type" : "header",
    "data" : {
        "text" : "Why Telegram is the best messenger",
        "level" : 2
    }
}
```

