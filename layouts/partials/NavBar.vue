<template>
  <div class="navBar">
    <div class="nav w-full flex justify-between items-center">
      <h3 class="logo">ALA</h3>
      <ul class="flex flex-row items-center nav-links">
        <li
          v-for="(link, index) in links"
          :key="index"
          class="nav-link lg:mr-8"
          @click="$nuxt.$emit('scroll-to', link.to)"
        >
          {{ link.name }}
        </li>
        <li>
          <a
            href="/Resume"
            target="_blank"
            title="Resume"
            class="button-outline"
            >Resume</a
          >
        </li>
      </ul>

      <ul id="sidebar" class="flex w-full flex-col items-center sidebar">
        <li
          v-for="(link, index) in links"
          :key="index"
          class="nav-link"
          @click="scrollTo(link.to)"
        >
          {{ link.name }}
        </li>
        <li>
          <a
            href="/Resume"
            target="_blank"
            title="Resume"
            class="button-outline"
            >Resume</a
          >
        </li>
      </ul>
      <div class="toggle open" v-if="!navToggle" @click="openNav">
        <inline-svg
          :src="require('@/assets/icons/menu.svg')"
          width="28"
          height="28"
          aria-label="Link"
        ></inline-svg>
      </div>
      <div class="toggle close" v-if="navToggle" @click="closeNav">
        <inline-svg
          :src="require('@/assets/icons/close.svg')"
          width="28"
          height="28"
          aria-label="Link"
        ></inline-svg>
      </div>
    </div>
    <div class="sidebar-menu"></div>
  </div>
</template>

<script>
import InlineSvg from "vue-inline-svg";
export default {
  name: "NavBar",
  components: {
    InlineSvg,
  },
  data() {
    return {
      navToggle: false,
      links: [
        {
          name: "Home",
          to: "hero",
        },
        {
          name: "About",
          to: "about",
        },
        {
          name: "Experience",
          to: "experience",
        },
        {
          name: "Projects",
          to: "projects",
        },
        {
          name: "Contact",
          to: "contact",
        },
      ],
    };
  },
  methods: {
    openNav() {
      this.navToggle = true;
      document.getElementById("sidebar").style.top = "-25px";
    },
    closeNav() {
      this.navToggle = false;
      document.getElementById("sidebar").style.top = "-500px";
    },
    scrollTo(section) {
      this.$nuxt.$emit("scroll-to", section);
      this.closeNav();
    },
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

.nav-links {
  gap: 25px;
}

.sidebar {
  display: none;
}

.nav-link {
  transition: 0.3s;
}

.nav-link:hover {
  color: var(--green);
}

.toggle {
  display: none;
}

@media screen and (max-width: 1200px) {
  .nav {
    top: 25px;
  }
  .nav-links {
    gap: 15px;
  }
}

@media screen and (max-width: 1024px) {
  .nav-links {
    display: none;
  }
  .sidebar {
    transition: 0.3s;
    position: absolute;
    display: flex;
    background: var(--background);
    top: -500px;
    left: 0;
    padding: 50px 0;
    gap: 25px;
  }
  .toggle {
    position: absolute;
    display: flex;
    top: 5%;
    right: 10%;
  }
}
</style>