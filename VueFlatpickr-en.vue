<template>
  <input type="text">
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
    new Flatpickr(this.$el, this.options)
  },
  mounted() {
    new Flatpickr(this.$el, this.options)
  }
}
</script>
