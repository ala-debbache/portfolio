<template>
  <div class="nav w-full flex justify-between items-center">
    <h3>ALA</h3>
    <ul class="flex items-center">
      <li v-for="(link, index) in links" :key="index" class="nav-link mr-8">
        <nuxt-link :to="link.to">{{ link.name }}</nuxt-link>
      </li>
      <li>
        <a href="/Resume" target="_blank" title="Resume" class="button-outline"
          >Resume</a
        >
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "NavBar",
  data() {
    return {
      links: [
        {
          name: "Home",
          to: "/",
        },
        {
          name: "About",
          to: "/about",
        },
        {
          name: "Experience",
          to: "/experience",
        },
        {
          name: "Projects",
          to: "/projects",
        },
        {
          name: "Contact",
          to: "/contact",
        },
      ],
    };
  },
};
</script>

<style>
.nav {
  position: absolute;
  top: 50px;
  left: 0;
  width: 100%;
  padding: 0 10%;
}

.nav-link {
  transition: 0.3s;
}

.nav-link:hover {
  color: var(--green);
}
</style>