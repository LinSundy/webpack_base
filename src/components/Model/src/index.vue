<template>
  <Dialog :visible="true" @close="close">
    <slot name="header"></slot>
    <slot></slot>
    <slot name="footer"></slot>
  </Dialog>
</template>
<script>
import {Dialog} from "element-ui"
export default {
  name: 'Model',
  components: {
    Dialog
  },
  methods: {
    close() {
      this.$emit("update:visible", false)
    }
  }
}
</script>