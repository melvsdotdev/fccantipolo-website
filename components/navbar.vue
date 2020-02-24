<template>
  <nav class="navbar is-primary is-transparent is-fixed-top" role="navigation" aria-label="navigation">
    <div class="container">
      <div class="navbar-brand">
        <nuxt-link to="/" class="navbar-item">
          <img class="logo" src="@/assets/images/fcc_primary_large.png" alt="freeCodeCamp">
          <h1 class="logo-suffix">
            | {{ city }}
          </h1>
        </nuxt-link>
        <a
          class="navbar-burger"
          role="button"
          aria-label="menu"
          aria-expanded="false"
          data-target="navMenu"
        >
          <span aria-hidden="true" />
          <span aria-hidden="true" />
          <span aria-hidden="true" />
        </a>
      </div>
      <div id="navMenu" class="navbar-menu">
        <div class="navbar-end">
          <nuxt-link to="/news" class="navbar-item">
            /news
          </nuxt-link>
          <nuxt-link to="/meetups" class="navbar-item">
            /meetups
          </nuxt-link>
          <nuxt-link to="/resources" class="navbar-item">
            /resources
          </nuxt-link>
          <nuxt-link to="/about" class="navbar-item">
            /about
          </nuxt-link>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  data () {
    return {
      city: this.$store.state.city
    }
  }
}
</script>
