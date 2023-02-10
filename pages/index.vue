<template>
  <div>
    <Hero ref="hero" />
    <About ref="about" />
    <Experience ref="experience" />
    <Projects ref="projects" />
    <Contact ref="contact" />
  </div>
</template>

<script>
export default {
  name: "IndexPage",
  methods: {
    scrollTo(section) {
      this.$refs[section].$el.scrollIntoView({ behavior: "smooth" });
    },
  },
  mounted() {
    this.$nuxt.$on("scroll-to", (section) => this.scrollTo(section));
  },
};
</script>
