<template>
  <span class="icon" v-html="path"></span>
</template>

<script>
import icons from '@/components/icons'
export default {
  props: {
    name: {
      type: String,
      default: ''
    }
  },
  computed: {
    path() {
      return icons[this.name]
    }
  }
}
</script>

<style lang="scss" scoped>
.icon {
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
