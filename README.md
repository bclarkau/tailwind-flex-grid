# Tailwind Flex Grid
Tailwind CSS Bootstrap 4 like columns plugin

## Flexbox grid

It exposes three configuration options:

- `columns`, for specifying all of the column sizes you'd like to generate
- `gutter`, for specifying the gutter the the row and columnns
- `variants`, for specifying which variants to generate

```js
module.exports = {
  // ...

  plugins: [
    // ...
    require('tailwind-flex-grid/grid')({
      columns: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12],
      gutter: 30,
      variants: ['responsive'],
    }),
  ],
}
```

With zero configuration, it will generate a row class, 1 to 12 columns, offsets, column ordering, gutter sizes and `responsive` variants for each new utility.

The plugin generates the following sets of classes:

- `.row`, for setting `display: flex` and `flex-wrap: wrap` on an element
- `.col-{size}`, for specifying the number of columns in the grid
- `.order-first`, for placing the element first in the row
- `.order-last`, for placing the element last in the row
- `.order-{size}`, for placing the element at specific places in the row
- `.offset-{size}`, for the margin-left offset for the element
- `.gutter-small`, for specifying a smaller half-size gutter in a `.row`.
- `.gutter-base`, for resetting the gutter back to the base size in a `.row`.
- `.gutter-large`, for specifying a larger double-size gutter in a `.row`.

### Using gutter classes

`.gutter-small`, `.gutter-base` and `.gutter-large` are useful in conjunction with Tailwind's responsive prefixes to change gutter spacing depending on screen width. eg:

```html
<div class="row gutter-small md:gutter-base xl:gutter-large">
```

## Installing
```js
npm install bclarkau/tailwind-flex-grid --save-dev
```
