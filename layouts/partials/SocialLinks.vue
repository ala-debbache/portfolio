<template>
  <div class="social-links flex flex-col">
    <a href="http://linkedin.com" target="_blank" class="link"
      ><inline-svg
        :src="require('@/assets/icons/linkedin.svg')"
        width="28"
        height="28"
        aria-label="Github"
      ></inline-svg
    ></a>
    <a href="http://github.com" target="_blank" class="link"
      ><inline-svg
        :src="require('@/assets/icons/github.svg')"
        width="28"
        height="28"
        aria-label="Github"
      ></inline-svg
    ></a>
    <a href="http://twitter.com" target="_blank" class="link"
      ><inline-svg
        :src="require('@/assets/icons/twitter.svg')"
        width="28"
        height="28"
        aria-label="Github"
      ></inline-svg
    ></a>
  </div>
</template>

<script>
import LinkedIn from "./icons/LinkedIn.vue";
import Github from "./icons/Github.vue";
import Twitter from "./icons/Twitter.vue";
import InlineSvg from "vue-inline-svg";
export default {
  name: "SocialLinks",
  components: {
    LinkedIn,
    Github,
    Twitter,
    InlineSvg,
  },
};
</script>

<style>
.social-links {
  position: fixed;
  top: 75vh;
  margin-left: -7%;
  gap: 25px;
}

.link * {
  transition: 0.3s;
}

.link * {
  stroke: var(--white) !important;
}
.link:hover * {
  stroke: var(--green) !important;
}

@media screen and (max-width: 1200px) {
  .link svg {
    width: 24px;
    height: 24px;
  }
}

@media screen and (max-width: 768px) {
  .social-links {
    display: none;
  }
}
</style>