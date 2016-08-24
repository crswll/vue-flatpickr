# vue-flatpickr
A Vue component that wraps the [Flatpickr](https://github.com/chmln/flatpickr).

Demo: [https://jrainlau.github.io/vue-flatpickr/](https://jrainlau.github.io/vue-flatpickr/)

## Install
```
npm install vue-flatpickr
```

## Usage
Enter one of your `.vue` file, load the instance `VueFlatpickr-en.vue` (or `VueFlatpickr-zh` for Chinese),  and the stylesheet `flatpickr.min.css`.
> Note that you have set the correct path, for example you might set the path as `../node_modules/vue-flatpickr/VueFlatpickr-en.vue` and so on.

```
<template>
  <vue-flatpickr></vue-flatpickr>
</template>

<script>
import VueFlatpickr from './VueFlatpickr-en'

export default {
  components: {
    VueFlatpickr
  }
}
</script>

<style>
@import './assets/flatpickr.min.css';
</style>
```

## Options
Use `props` to pass the **options object** to `vue-flatpickr`. The options are same to the [official document](https://chmln.github.io/flatpickr/#options). Here is an example below:
```
<!-- template -->
<vue-flatpickr :options="fpOptions"></vue-flatpickr>

<!-- script -->
data() {
    return {
      fpOptions: {
        enableTime: true
      }
    }
  }
```

## Data binding
The  `<vue-flatpick></vue-flatpickr>` tag could be use as a normal `<input>` tag, which you can use `v-model` to bind data withVue model:
```
<vue-flatpickr v-model='date'></vue-flatpickr>
```

## Themes
`vue-flatpickr` supports all the offical themes, all you need to do is to pick up the one you like:
- `flatpickr.min.css`
- `flatpickr.confetti.min.css`
- `flatpickr.dark.min.css`
- `flatpickr.material_blue.min.css`
- `flatpickr.material_green.min.css`
- `flatpickr.material_orange.min.css`
- `flatpickr.material_red.min.css`

## Lisense
MIT