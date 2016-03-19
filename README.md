# &lt;kwc-toolbar&gt;

> A web component for toolbar management

## Install

Install the component using [Bower](http://bower.io/):

```sh
$ bower install kwc-toolbar --save
```

Or [download as ZIP](https://github.com/successk/kwc-toolbar/archive/master.zip).

## Usage

1 – Import polyfill:

```html
<script src="bower_components/webcomponentsjs/webcomponents-lite.min.js"></script>
```

2 – Import custom element:

```html
<link rel="import" href="bower_components/kwc-toolbar/kwc-toolbar.html">
```

3 – Start using it!

```html
<kwc-toolbar iconsize="50">
    <kwc-toolbar-group iconsize="30">
      <kwc-toolbar-item name="bold" src="bold.png" info="Set the text bold" iconsize="20"></kwc-toolbar-item>
      <kwc-toolbar-item name="italic" src="italic.png" info="Set the text italic"></kwc-toolbar-item>
    </kwc-toolbar-group>
    <kwc-toolbar-group>
      <kwc-toolbar-item name="copy" src="copy.png" info="Copy text"></kwc-toolbar-item>
      <kwc-toolbar-item name="paste" src="paste.png" info="Paste text"></kwc-toolbar-item>
    </kwc-toolbar-group>
    <kwc-toolbar-group>
      <kwc-toolbar-item name="duplicate" info="Duplicate the text">Duplicate</kwc-toolbar-item>
    </kwc-toolbar-group>
  </kwc-toolbar>
```

## Options

### kwc-toolbar

Attribute   | Options         | Default      | Description
---         | ---             | ---          | ---
`iconsize`  | *number*        | `null`       | Size of icons in this toolbar, if groups and items does not redefine it

### kwc-toolbar-group

Attribute   | Options         | Default      | Description
---         | ---             | ---          | ---
`iconsize`  | *number*        | `null`       | Size of icons in this group, if items does not redefine it
`gid`       | *String*        | `null`       | *Read only*, id of the kwc-group (different of id kept for developer use)

### kwc-toolbar-item

Attribute   | Options         | Default      | Description
---         | ---             | ---          | ---
`name`      | *string*        | `null`       | Name of the item and the toolbar event on click.
`src`       | *string*        | `null`       | Url of the icon image
`iconsize`  | *number*        | `null`       | Size of icon of this item if defined with src
`info`      | *string*        | `null`       | Text informing the user about current item

## Children

### kwc-toolbar

Selector | Description
---      | ---
`*`      | Content of the toolbar, should contain `kwc-toolbar-*` only.

### kwc-toolbar-group

Selector | Description
---      | ---
`*`      | Content of the group, should contain `kwc-toolbar-items` only.

### kwc-toolbar-item

Selector | Description
---      | ---
`*`      | Content of the item, displayed only when src is not defined.

## Methods

Method        | Parameters   | Returns     | Description
---           | ---          | ---         | ---
None          | -            | -           | -

## Events

Event     | Detail   | Description
---       | ---      | ---
None      | -        | -

When the user click on a `kwc-toolbar-item`, an event with the component name will be triggered.

For instance, a click on `<kwc-toolbar-item name="xxx">` will trigger the event `xxx`;

## Styles

Name  | Default   | Description
---   | ---       | --
None  | -         | -

## Development

In order to run it locally you'll need to fetch some dependencies and a basic server setup.

1 – Install [bower](http://bower.io/) & [polyserve](https://npmjs.com/polyserve):

```sh
$ npm install -g bower polyserve
```

2 – Install local dependencies:

```sh
$ bower install
```

3 – Start development server and open `http://localhost:8080/components/kwc-toolbar/`.

```sh
$ polyserve
```

## History

For detailed changelog, check [Releases](https://github.com/successk/kwc-toolbar/releases).

## License

MIT