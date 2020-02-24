<template>
  <div>
    <hero />
  </div>
</template>

<script>
import hero from '@/components/home/hero.vue'

export default {
  components: {
    hero
  },
  mounted () {
    this.$nextTick(() => {
      this.$nuxt.$loading.start()
      setTimeout(() => this.$nuxt.$loading.finish(), 500)
    })
  },
  head () {
    return {
      title: `freeCodeCamp ${this.$store.state.city} | Learn to code with us`
    }
  }
}
</script>
