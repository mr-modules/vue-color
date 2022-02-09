# vue-color fork

[![npm](https://img.shields.io/npm/v/vue-color.svg)](https://www.npmjs.com/package/vue-color)

## [Live demo](http://xiaokaike.github.io/vue-color/)

## Installation

### NPM
```bash
$ npm install mr-vue-color
```
### Yarn
```bash
$ yarn add mr-vue-color
```

### ES6
```js
import ColorPicker from 'mr-vue-color/src/component/Simple.vue'

new Vue({
  components: {
    ColorPicker
  }
})
```
## Usage

```js

var colors = {
  hex: '#194d33',
  hex8: '#194D33A8',
  hsl: { h: 150, s: 0.5, l: 0.2, a: 1 },
  hsv: { h: 150, s: 0.66, v: 0.30, a: 1 },
  rgba: { r: 25, g: 77, b: 51, a: 1 },
  a: 1
}
// or
var colors = '#194d33'
// or
var colors = '#194D33A8'
// or 
var colors = { h: 150, s: 0.66, v: 0.30 }
// or 
var colors = { r: 255, g: 0, b: 0 }
// etc...

new Vue({
  el: '#app',
  components: {
    ColorPicker
  },
  data () {
    return {
      colors
    }
  }
})

```

`colors` accepts either a string of a hex color '#333' or a object of rgb or hsl values `{ r: 51, g: 51, b: 51 }` or `{ h: 0, s: 0, l: .10 }`, whatever [tinycolor2](https://www.npmjs.com/package/tinycolor2) accepts as an input.

```html
<!-- suppose you have the data 'colors' in your component -->
<color-picker v-model="colors" />
```

OR

```html
<color-picker :value="colors" @input="updateValue"></color-picker>
```

In some cases you can give the component a predefined set of colors with the property `presetColors`, by simply passing it an array with the color values as strings in any css compatible format.

```html
<color-picker 
  @input="updateValue"
  :value="colors"
  :preset-colors="[ 
    '#f00', '#00ff00', '#00ff0055', 'rgb(201, 76, 76)', 'rgba(0,0,255,1)', 'hsl(89, 43%, 51%)', 'hsla(89, 43%, 51%, 0.6)'
  ]"
/>
```

## License

vue-color is licensed under [The MIT License](LICENSE).
