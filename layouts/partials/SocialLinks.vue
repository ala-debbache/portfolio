<template>
  <div class="social-links">
    <a href="http://linkedin.com" target="_blank" class=""
      ><LinkedIn class="link"
    /></a>
    <a href="http://github.com" target="_blank" class="link"
      ><Github class="link"
    /></a>
    <a href="http://twitter.com" target="_blank" class="link"
      ><Twitter class="link"
    /></a>
  </div>
</template>

<script>
import LinkedIn from "./icons/LinkedIn.vue";
import Github from "./icons/Github.vue";
import Twitter from "./icons/Twitter.vue";
export default {
  name: "SocialLinks",
  components: {
    LinkedIn,
    Github,
    Twitter,
  },
};
</script>

<style>
.social-links {
  position: fixed;
  top: 70%;
  margin-left: -100px;
}
</style>