<template>
  <div class="app">
    <NavBar />
    <Nuxt />
    <SocialLinks />
    <div class="w-ful text-center footer">
      Designed & Built by Ala Eddine Debbache
    </div>
    <div class="bg-gradient"></div>
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
.footer {
  margin-top: 200px;
  font-size: 16px;
}
</style>