<template>
  <input type="text" id="vue-flatpickr">
</template>

<script>
import Flatpickr from './assets/flatpickr-en.js'

export default {
  props: {
    options: {
      type: Object
    }
  },
  watch: {
    options: {
      handler() {
        this.newFlatpickr()
      },
      deep: true
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
