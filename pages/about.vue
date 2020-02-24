<template>
  <div>
    <soon />
  </div>
</template>

<script>
import soon from '@/components/soon.vue'

export default {
  components: {
    soon
  },
  head () {
    return {
      title: `About | freeCodeCamp ${this.$store.state.city}`
    }
  }
}
</script>
