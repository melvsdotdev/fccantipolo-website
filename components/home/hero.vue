<template>
  <section class="hero is-medium is-primary has-background">
    <img :src="heroImage" alt="" class="hero-background">
    <div class="hero-overlay" />
    <div class="hero-body">
      <div class="container">
        <div class="columns">
          <div class="column is-half">
            <h1 class="title">
              Learn to Code with us!
            </h1>
            <h2 class="subtitle">
              We are a local community and study group learning to code through
              <a :href="fcc" target="_blank" rel="noopener noreferrer">
                freeCodeCamp.org
              </a>
            </h2>
            <div class="field">
              <p class="control">
                <a
                  target="_blank"
                  rel="noopener noreferrer"
                  :href="facebookGroup"
                  class="button is-primary is-rounded is-inverted"
                >
                  Join the community
                </a>
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data () {
    return {
      city: this.$store.state.city,
      facebookGroup: this.$store.state.facebookGroup,
      heroImage: this.$store.state.heroImage,
      fcc: `https://freecodecamp.org?ref=freeCodeCamp.${this.$store.state.city}`
    }
  }
}
</script>
