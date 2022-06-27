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

It works just like normal tailwind borders, by adding `text-border-[width]` and `text-border[color]`

The width is limited to 2px max. For values above this it gets ugly. Default width is 1px.

The plugin uses the theme colors, so no limitations here.

### Example

<h1 class="text-border text-border-red">Hello world</h1>
