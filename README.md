# preact-hashtabs

A minimal `<Tabs />` component for
[preact](https://github.com/developit/preact) based on
`window.location.hash`, so it is **not suitable** for complicated use of nested
tabs, and its functionality is yet very simple.

## Properties

### `tabdefault`

Activate a tab with `tabdefault` if no hash in current locaion.  If there are
multiple default tabs, the last one will be enabled.

### `label`

`href` and text content for the link (`<a />`) of a tab, e.g. `{foo: 'Foo'}`.

### `activeClassName`

A class name to append in the active tab's `classList`.

## Example

[anqurvanillapy.github.io/preact-hashtabs](https://anqurvanillapy.github.io/preact-hashtabs)

```js
import { h, render } from 'preact'
import { Tabs, Tab } from 'preact-hashtabs'

const App = () => (
  <Tabs>
    <Tab
      tabdefault
      id='foo'
      label={{tab0: 'Tab 0'}}
      activeClassName='active'
    >
      <ul><li>foo</li></ul>
    </Tab>
    <Tab label={{tab1: 'Tab 1'}} activeClassName='active'>
      <ul><li>bar</li></ul>
    </Tab>
    <Tab label={{tab2: 'Tab 2'}} activeClassName='active'>
      <ul><li>baz</li></ul>
    </Tab>
    <Tab label={{tab3: 'Tab 3'}} activeClassName='active'>
      <ul><li>qux</li></ul>
    </Tab>
  </Tabs>
)

render(<App />, document.body)
```

## Install

```bash
$ npm i -s preact-hashtabs
```

## License

ISC
