<template>
  <footer class="footer">
    <div class="container">
      <div class="columns">
        <div class="column is-6">
          <img class="seal" src="@/assets/images/fcc_secondary_large.png" alt="freeCodeCamp">
          <p>
            <a :href="facebookGroup" target="_blank" rel="noopener noreferrer">freeCodeCamp {{ city }}</a> is not affiliated with or endorsed by <a :href="fcc" target="_blank" rel="noopener noreferrer">freeCodeCamp.org</a>.
            We are an independent local study group/community learning to code through <a :href="fcc" target="_blank" rel="noopener noreferrer">freeCodeCamp.org</a>.
          </p>
          <p>
            All trademarks and other contents appearing in this site are property of it's respective owners.
          </p>
        </div>
        <div class="column is-1" />
        <div class="column is-2">
          <h1 class="title is-5">
            Sitemap
          </h1>
          <ul>
            <li>
              <nuxt-link to="/news">
                /news
              </nuxt-link>
            </li>
            <li>
              <nuxt-link to="/meetups">
                /meetups
              </nuxt-link>
            </li>
            <li>
              <nuxt-link to="/resources">
                /resources
              </nuxt-link>
            </li>
            <li>
              <nuxt-link to="/about">
                /about
              </nuxt-link>
            </li>
          </ul>
        </div>
        <div class="column is-1" />
        <div class="column is-2">
          <h1 class="title is-5">
            freeCodeCamp
          </h1>
          <ul>
            <li>
              <a href="https://www.freecodecamp.org/news" target="_blank" rel="noopener noreferrer">
                /news
              </a>
            </li>
            <li>
              <a href="https://www.freecodecamp.org/forum" target="_blank" rel="noopener noreferrer">
                /forum
              </a>
            </li>
            <li>
              <a href="https://www.freecodecamp.org/learn" target="_blank" rel="noopener noreferrer">
                /learn
              </a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  data () {
    return {
      city: this.$store.state.city,
      facebookGroup: this.$store.state.facebookGroup,
      fcc: `https://freecodecamp.org?ref=freeCodeCamp.${this.$store.state.city}`
    }
  }
}
</script>
