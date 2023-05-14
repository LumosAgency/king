<template>
  <div id="navigation" class="navigation" aria-expanded="false">
    <div class="navigation__wrapper">
      <button class="navigation__toggle" @click="toggleNav">
        <span class="navigation__toggle-icon"></span>
        <span class="navigation__toggle-label" aria-hidden="true">Menu</span>
      </button>
      <nav
        aria-controls="navigation__list"
        id="navigation__list"
        class="navigation__list"
        :aria-expanded="isNavOpen ? 'true' : 'false'"
        :aria-hidden="!isNavOpen"
      >
        <ul class="navigation__items">
          <li class="navigation__item">
            <nuxt-link to="/" class="navigation__link">Home</nuxt-link>
          </li>
          <li class="navigation__item">
            <nuxt-link to="/about" class="navigation__link">About Us</nuxt-link>
          </li>
          <li class="navigation__item">
            <nuxt-link to="/stay" class="navigation__link">Stay</nuxt-link>
          </li>
          <li class="navigation__item">
            <nuxt-link to="/grooming" class="navigation__link"
              >Grooming</nuxt-link
            >
          </li>
          <li class="navigation__item">
            <nuxt-link to="/party" class="navigation__link">Party</nuxt-link>
          </li>
        </ul>
      </nav>
    </div>
    <div class="navigation__overlay"></div>
  </div>
</template>
  
  <script>
export default {
  name: 'Navigation',
  data() {
    return {
      isNavOpen: false,
    }
  },
  methods: {
    toggleNav() {
      this.isNavOpen = !this.isNavOpen
      this.$nextTick(() => {
        const nav = document.getElementById('navigation')
        const navList = document.getElementById('navigation__list')
        if (this.isNavOpen) {
          nav.setAttribute('aria-expanded', 'true')
          navList.setAttribute('aria-expanded', 'true')
        } else {
          nav.setAttribute('aria-expanded', 'false')
          navList.setAttribute('aria-expanded', 'false')
        }
      })
    },
  },
  watch: {
    $route() {
      const nav = document.getElementById('navigation')
      const navList = document.getElementById('navigation__list')
      nav.setAttribute('aria-expanded', 'false')
      navList.setAttribute('aria-expanded', 'false')
    },
  },
}
</script>