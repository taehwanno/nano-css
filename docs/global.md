# `:global` Addon

`global` addon allows to inject global CSS. It introduces a `:global` selector that can be
used in any CSS-like object and exposes `global()` function for convenience.

Use `:global` selector.

```js
const className = nano.put('.foo', {
    color: 'red',
    '.nested': {
        fontWeight: 'bold'
    },
    ':global': {
        '.global_class': {
            border: '1px solid red'
        }
    }
});
```

This results in:

```css
.foo {
    color: red;
}
.foo .nested {
    font-weight: bold;
}
.global_class {
    border: 1px solid red;
}
```

Use `global()` function to emit global CSS.

```js
nano.global({
    '.global_class': {
        border: '1px solid red'
    }
});
```


## Installation

Simply install `global` addon. Read more about the [Addon Installation](./Addons.md#addon-installation).
