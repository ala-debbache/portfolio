<template>
  <section class="contact w-full">
    <div class="section-header">
      <h2 class="section-title">Contact</h2>
      <h1 class="section-title-stroke">Contact</h1>
    </div>
    <div class="flex justify-between detail">
      <p class="description">
        I’m currently looking for new opportunities, my inbox is always open.
        Whether you have a question or just want to say hi.
      </p>
      <ul class="flex flex-col infos">
        <li class="flex info">
          <inline-svg
            :src="require('@/assets/icons/map.svg')"
            width="28"
            height="28"
            aria-label="Github"
          ></inline-svg>
          <span>Algeria Batna</span>
        </li>
        <li class="flex info">
          <inline-svg
            :src="require('@/assets/icons/email.svg')"
            width="28"
            height="28"
            aria-label="Github"
          ></inline-svg>
          <span>debbacheala2@gmail.com</span>
        </li>
        <li class="flex info">
          <a href="http://linkedin.com" target="_blank" class="contact-link"
            ><inline-svg
              :src="require('@/assets/icons/linkedin.svg')"
              width="28"
              height="28"
              aria-label="Github"
            ></inline-svg
          ></a>
          <a href="http://github.com" target="_blank" class="contact-link"
            ><inline-svg
              :src="require('@/assets/icons/github.svg')"
              width="28"
              height="28"
              aria-label="Github"
            ></inline-svg
          ></a>
          <a href="http://twitter.com" target="_blank" class="contact-link"
            ><inline-svg
              :src="require('@/assets/icons/twitter.svg')"
              width="28"
              height="28"
              aria-label="Github"
            ></inline-svg
          ></a>
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
import InlineSvg from "vue-inline-svg";

export default {
  name: "Contact",
  components: {
    InlineSvg,
  },
};
</script>

<style>
.contact {
  margin-top: 200px;
}
.infos {
  gap: 15px;
}
.info {
  gap: 15px;
}

@media screen and (max-width: 1200px) {
  .contact {
    margin-top: 150px;
  }
  .contact-link svg {
    width: 24px;
    height: 24px;
  }
  .info svg {
    width: 24px;
    height: 24px;
  }
}

@media screen and (max-width: 1024px) {
  .detail {
    flex-direction: column;
    gap: 30px;
  }
}

@media screen and (max-width: 768px) {
  .contact {
    margin-top: 100px;
  }
}
</style>