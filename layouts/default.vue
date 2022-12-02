<template>
  <div class="app">
    <NavBar />
    <Nuxt />
    <SocialLinks />
    <Footer />
    <div class="bg-gradient"></div>
  </div>
</template>

<script>
import NavBar from "./partials/NavBar.vue";
import SocialLinks from "./partials/SocialLinks.vue";
import Footer from "./partials/Footer.vue";
export default {
  name: "Layout",
  components: { NavBar, SocialLinks, Footer },
};
</script>

<style>
.app {
  max-width: 100%;
  overflow: hidden !important;
  padding: 0 10%;
  padding-bottom: 20px;
  background: url("../assets/images/Pattern.png");
  /* background-size: 0%; */
  background-position: top right;
  background-repeat: no-repeat;
  background-attachment: scroll;
  background-size: 45%;
}
.bg-gradient {
  position: fixed;
  width: 100%;
  height: 100%;
  left: -50%;
  bottom: -40%;
  border-radius: 50%;
  background: rgba(9, 88, 133, 0.8);
  filter: blur(150px);
  z-index: -1;
}

@media screen and (max-width: 1200px) {
  .app {
    background-size: 60%;
  }
}

@media screen and (max-width: 768px) {
  .app {
    background-size: 80%;
  }
}
</style>