<template>
  <div class="footer">
    <div class="w-ful text-center footer">
      Designed & Built by Ala Eddine Debbache
    </div>
    <div class="flex justify-center footer-links">
      <a href="http://linkedin.com" target="_blank" class="footer-link"
        ><inline-svg
          :src="require('@/assets/icons/linkedin.svg')"
          width="18"
          height="18"
          aria-label="Github"
        ></inline-svg
      ></a>
      <a href="http://github.com" target="_blank" class="footer-link"
        ><inline-svg
          :src="require('@/assets/icons/github.svg')"
          width="18"
          height="18"
          aria-label="Github"
        ></inline-svg
      ></a>
      <a href="http://twitter.com" target="_blank" class="footer-link"
        ><inline-svg
          :src="require('@/assets/icons/twitter.svg')"
          width="18"
          height="18"
          aria-label="Github"
        ></inline-svg
      ></a>
    </div>
  </div>
</template>

<script>
import InlineSvg from "vue-inline-svg";
export default {
  name: "Footer",
  components: {
    InlineSvg,
  },
};
</script>

<style>
.footer {
  margin-top: 100px;
  font-size: 16px;
}
.footer-links {
  margin-top: 10px;
  gap: 10px;
  display: none;
}
.footer-link * {
  stroke: var(--white);
}

@media screen and (max-width: 768px) {
  .footer-links {
    display: flex;
  }
}
</style>