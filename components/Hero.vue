<template>
  <section class="hero">
    <p class="margin-bottom">Hi, my name is</p>
    <h1 class="title">Ala Eddine</h1>
    <h1 class="title stroke margin-bottom">
      Full stack web <br />
      developer
    </h1>
    <p class="description margin-bottom">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
      tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
      veniam
    </p>
    <a href="#" target="_blank" class="button">Say Hi</a>
  </section>
</template>

<script>
export default {
  name: "Hero",
};
</script>

<style>
.hero {
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.title {
  color: var(--green);
  line-height: 105%;
}
.stroke {
  -webkit-text-fill-color: transparent;
  -webkit-text-stroke: 2px;
  line-height: 85%;
}
</style>