<template>
  <div class="footer">
    <div class="footer__left">
      <h4>
        <nuxt-link to="/" class="navigation__link">Cat's Meow Resort</nuxt-link>
      </h4>
      <ul class="footer__social">
        <li><a href="#" target="_blank" class="footer__social__insta"></a></li>
        <li>
          <a href="#" target="_blank" class="footer__social__facebook"></a>
        </li>
        <li>
          <a href="#" target="_blank" class="footer__social__twitter"></a>
        </li>
      </ul>
    </div>
    <div class="footer__right">
      <div>
        <p>Company</p>
        <ul>
          <li>
            <nuxt-link to="/about" class="navigation__link">About Us</nuxt-link>
          </li>
          <li>
            <nuxt-link to="/stay" class="navigation__link">Stay</nuxt-link>
          </li>
          <li>
            <nuxt-link to="/grooming" class="navigation__link"
              >Grooming</nuxt-link
            >
          </li>
        </ul>
      </div>
      <div>
        <p>Support</p>
        <ul>
          <li><nuxt-link to="/faq" class="navigation__link">FAQ</nuxt-link></li>
          <li>
            <nuxt-link to="/privacy" class="navigation__link"
              >Privacy</nuxt-link
            >
          </li>
          <li>
            <nuxt-link to="/terms" class="navigation__link"
              >Terms & Policy</nuxt-link
            >
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>