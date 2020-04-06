# Vue Time Picker

[![Build Status](https://travis-ci.org/tylergrinn/vue-time-picker.svg?branch=master)](https://travis-ci.org/tylergrinn/vue-time-picker)

NOTE: This fork contains Voxgig-specific customizations


## [DEMO](http://vue-time-picker.surge.sh/demo.html)

Simple, no nonsense time picker built and optimized for Vue.

![mobile](docs/time-picker-mobile.gif)
![desktop](docs/time-picker-desktop.gif)

## Installation

### Yarn
```
yarn add -D @tygr/vue-time-picker
```
```js
import TimePicker from '@tygr/vue-time-picker'

export default {
  components: {
    TimePicker,
  }
}
```

### Browser
```html
<script type="text/javascript" src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
<script src="https://unpkg.com/@tygr/vue-time-picker/dist/vue-time-picker.min.js" charset="utf-8"></script>
<script>
  Vue.use(TimePicker)
</script>
```

* Charset attribute required

## Usage

```html
<time-picker v-model="time"></time-picker>
```

```js
export default {
  data: () => ({
    time: ''
  })
}
```

Time format is `h:mm A`

## Props

| prop         | type   | default                               | description                                     |
| ------------ | ------ | ------------------------------------- | ----------------------------------------------- |
| am-color     | string | 'green'                               | Color of the slider when 'AM' is chosen         |
| pm-color     | string | 'blue'                                | Color of the slider when 'PM' is chosen         |
| value        | string | '12:00 AM'                            | The value of the time picker. (used by v-model) |
| mobile-query | string | 'only screen and (max-width : 839px)' | Media query used to check if mobile user        |

## Events

| event | payload | description                     |
| ----- | ------- | ------------------------------- |
| input | string  | Time selected (used by v-model) |
