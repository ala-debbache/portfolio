<template>
  <div class="app">
    <NavBar />
    <Nuxt />
    <SocialLinks />
    <div class="w-ful text-center footer">
      Designed & Built by Ala Eddine Debbache
    </div>
  </div>
</template>

<script>
import NavBar from "./partials/NavBar.vue";
import SocialLinks from "./partials/SocialLinks.vue";
export default {
  name: "Layout",
  components: { NavBar, SocialLinks },
};
</script>

<style>
.app {
  padding: 0 10%;
  padding-bottom: 20px;
  background: url("../assets/images/background.png"),
    url("../assets/images/Pattern.png");
  /* background-size: 0%; */
  background-position: 0 0, top right;
  background-repeat: no-repeat;
  background-attachment: fixed, scroll;
  background-size: auto, 45%;
}
.footer {
  margin-top: 200px;
  font-size: 16px;
}
</style>