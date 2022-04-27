<template>
    <div 
      v-html="compiledMarkdown"
      :text="text"
    />
</template>
<script>
import { richmd } from 'richmd'

export default {
  name: "Richmd",
  props: {
    text: {
      type: String,
      default: "",
      require: true,
    },
    className: {
      type: String,
      default: "",
    },
    id: {
      type: String,
      default: "",
    },
  },
  data() {
    return {
      markdownText: ''
    }
  },
  computed: {
    compiledMarkdown () {
      return richmd(this.markdownText)
    }
  },
}
</script>
<style>
@import 'richmd/richmd.css';
</style>
