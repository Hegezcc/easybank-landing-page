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
    </nav>
    <div class="bottom">
      <InviteButton />
      <p class="copy">© Easybank. All Rights Reserved</p>
    </div>
  </footer>
</template>
<style scoped lang="scss">
@use '@/assets/base.scss' as *;

footer {
  background-color: var(--dark-blue);
  color: var(--white);
  padding: 2rem;
  font-size: 0.8rem;

  a {
    color: var(--white);

    &:hover {
      color: var(--lime-green);
    }
  }
}

ul {
  margin: 1rem 0;
}

li {
  margin: 0.5rem;
}

.social {
  display: flex;
  justify-content: center;
}

.invite-button {
  margin: 1rem 0;
}

.copy {
  color: var(--grayish-blue);
}

@media screen and (min-width: $desktop-min) {
  footer {
    display: flex;
    justify-content: space-between;
  }

  .logo {
    text-align: center;
  }

  .links {
    display: flex;
    height: 7rem;
    flex-direction: column;
    flex-wrap: wrap;
  }

  .bottom {
    text-align: right;
  }

}
</style>