# Text borders in tailwind

A plugin to add text-border in tailwind.

It uses text-shadows under the hood, which act as 1px or 2px border (if thicker, things get ugly)

Works as simple as normal borders.

## Installation

Install the plugin from npm:
`npm install -D @tailwindcss-text-border`

Then add the plugin to your tailwind.config.js file:

```
module.exports = {
  theme: {
    // ...
  },
  plugins: [
    require('tailwindcss-text-border'),
    // ...
  ],
}
```

## Basic usage

It works just like normal tailwind borders, by adding `text-border-[width]` and `text-border-[color]`

The width is limited to 2px max. For values above this it gets ugly. Default width is 1px.

The plugin uses the theme colors, so no limitations here.

### Example 1

`<h1 class="text-border text-border-red">Hello world</h1>`

### Example 2

`<h1 class="text-border-2 text-border-yellow">Hello world</h1>`

## ⚠️ Warning ⚠️

The plugin relies on the following function for getting the colors from the theme:
`const flattenColorPalette = require('tailwindcss/lib/util/flattenColorPalette').default`

This can potentially lead to future problems. Check [this github repo](https://github.com/tailwindlabs/tailwindcss/discussions/8598) for more information.

Tips on how to fix this are welcomed!
