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
      <kwc-toolbar-select name="font" label="Font family" value="{{font}}" info="Select the font family for the text">
        <paper-item value="arial" style="font-family: Arial">Arial</paper-item>
        <paper-item value="courier new" style="font-family: 'Courier New'">Courier New</paper-item>
        <paper-item value="times new roman" style="font-family: 'Times New Roman'">Times New Roman</paper-item>
      </kwc-toolbar-select>
    </kwc-toolbar-group>
    <kwc-toolbar-group stateful state="{{align}}">
      <kwc-toolbar-item name="left" info="Align the text to the left">Left</kwc-toolbar-item>
      <kwc-toolbar-item name="center" info="Center the text">Center</kwc-toolbar-item>
      <kwc-toolbar-item name="right" info="Align the text to the right">Right</kwc-toolbar-item>
      <kwc-toolbar-item name="justify" info="Justify the text">Justify</kwc-toolbar-item>
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
`stateful`  | *Boolean*       | `false`      | If true, `kwc-toolbar-item` will act as radio buttons
`state`     | *String*        | `null`       | The value of selected item when group is `stateful`

### kwc-toolbar-item

Attribute   | Options         | Default      | Description
---         | ---             | ---          | ---
`name`      | *string*        | `null`       | Name of the item and the toolbar event on click.
`src`       | *string*        | `null`       | Url of the icon image
`iconsize`  | *number*        | `null`       | Size of icon of this item if defined with src
`info`      | *string*        | `null`       | Text informing the user about current item

### kwc-toolbar-select

Attribute   | Options         | Default      | Description
---         | ---             | ---          | ---
`name`      | *string*        | `null`       | Name of the item and the toolbar event on click
`label`     | *string*        | `null`       | Label to display when no value is selected
`info`      | *string*        | `null`       | Text informing the user about current item
`value`     | *string*        | `null`       | Value of the select

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

### kwc-toolbar-select

Selector | Description
---      | ---
`*`      | Options of the select. Should be `<paper-item>` elements with a `value` attribute.

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