<template>
    <div 
      v-html="compiledMarkdown"
      :text="text"
    />
</template>
<script>
import { richmd } from 'richmd'
import 'richmd/richmd.css'

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
