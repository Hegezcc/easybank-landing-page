<script setup>
import InviteButton from './InviteButton.vue'
</script>
<template>
  <footer>
    <div class="logo">
      <img src="@/assets/images/logo-inverted.svg" alt="Easybank" />
      <ul class="social">
        <li><a href="#"><img src="@/assets/images/icon-facebook.svg" /></a></li>
        <li><a href="#"><img src="@/assets/images/icon-youtube.svg" /></a></li>
        <li><a href="#"><img src="@/assets/images/icon-twitter.svg" /></a></li>
        <li><a href="#"><img src="@/assets/images/icon-pinterest.svg" /></a></li>
        <li><a href="#"><img src="@/assets/images/icon-instagram.svg" /></a></li>
      </ul>
    </div>
    <nav>
      <ul class="links">
        <li><a href="#">About Us</a></li>
        <li><a href="#">Contact</a></li>
        <li><a href="#">Blog</a></li>
        <li><a href="#">Careers</a></li>
        <li><a href="#">Support</a></li>
        <li><a href="#">Privacy Policy</a></li>
      </ul>
      <InviteButton />
    </nav>
    <p class="copy">© Easybank. All Rights Reserved</p>

    <div class="attribution">
      Challenge by <a href="https://www.frontendmentor.io?ref=challenge" target="_blank">Frontend Mentor</a>. 
      Coded by <a href="#">Your Name Here</a>.
    </div>
  </footer>
</template>
<style scoped lang="scss">

footer {
  background-color: var(--dark-blue);
  color: var(--white);

  a {
    color: var(--white);

    &:hover {
      color: var(--lime-green);
    }
  }
}

.attribution {
  font-size: 11px;
  text-align: center;

  a {
    color: hsl(228, 45%, 44%);
  }
}

</style>