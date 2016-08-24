<template>
  <input type="text" id="vue-flatpickr">
</template>

<script>
import Flatpickr from './assets/flatpickr-en.js'

export default {
  props: {
    options: {
      type: Object,
      default: () => {}
    }
  },
  ready() {
    new Flatpickr(document.querySelector('#vue-flatpickr'), this.options)
  },
  mounted() {
    new Flatpickr(document.querySelector('#vue-flatpickr'), this.options)
  }
}
</script>
