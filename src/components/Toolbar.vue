<template>
  <div class="toolbar">
    <button class="toolbar-button">New</button>
    <button class="toolbar-button">Delete</button>
    <multiselect v-model="value" :options="options"></multiselect>
  </div>
</template>

<style src="vue-multiselect/dist/vue-multiselect.min.css"></style>

<script>
import Multiselect from 'vue-multiselect'


export default {
  name: 'toolbar',
  components: { Multiselect },
  data () {
      return {
        value: null,
        options: ['list', 'of', 'options', 'another', 'fifth']
      }
    }
}
</script>