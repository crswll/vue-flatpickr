<template>
  <input type="text" :data-selector="selector">
</template>

<script>
import Flatpickr from './assets/flatpickr-zh.js'

export default {
  computed: {
    selector() {
      let t = ''
      for(let i = 0; i < 15; i++) { 
          t += Math.floor(Math.random() * 10) 
      }
      return 'vue-flatpickr-' + t
    }
  },
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
    new Flatpickr(document.querySelector(`[data-selector=${this.selector}]`), this.options)
  },
  mounted() {
    new Flatpickr(document.querySelector(`[data-selector=${this.selector}]`), this.options)
  }
}
</script>
