<template>
  <section class="projects w-full">
    <div class="section-header">
      <h2 class="section-title">Projects</h2>
      <h1 class="section-title-stroke">Projects</h1>
    </div>
    <div class="flex flex-col projects-list">
      <div
        v-for="(project, index) in projects"
        :key="index"
        class="flex justify-between project"
      >
        <div class="project-details">
          <h3 class="project-title">{{ project.title }}</h3>
          <p class="project-description">
            {{ project.description }}
          </p>
          <h3 class="tech-stack">Tech Stack</h3>
          <div class="flex flex-wrap project-tech-stack">
            <span
              v-for="(tech, index) in project.techStack"
              :key="index"
              class="tech"
              >{{ tech }}</span
            >
          </div>
          <div class="flex links">
            <a :href="project.github" target="_blanck">
              <inline-svg
                :src="require('@/assets/icons/github.svg')"
                width="28"
                height="28"
                aria-label="Github"
              ></inline-svg
            ></a>
            <a :href="project.link" target="_blanck">
              <inline-svg
                :src="require('@/assets/icons/link.svg')"
                width="28"
                height="28"
                aria-label="Link"
              ></inline-svg
            ></a>
          </div>
        </div>
        <div class="project-image">
          <img
            :src="require(`@/assets/images/projects/${project.image}`)"
            :alt="project.title + ' image'"
          />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import InlineSvg from "vue-inline-svg";
export default {
  name: "Projects",
  components: {
    InlineSvg,
  },
  data() {
    return {
      projects: [
        {
          title: "OSMS",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam",
          image: "osms.png",
          techStack: [
            "Vue JS",
            "Tailwind CSS",
            "Electron JS",
            "Node JS",
            "Bookshelf JS",
            "MySQL",
          ],
          github: "https://github.com",
          link: "https://google.com",
        },
        {
          title: "OSMS",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam",
          image: "osms.png",
          techStack: [
            "Vue JS",
            "Tailwind CSS",
            "Electron JS",
            "Node JS",
            "Bookshelf JS",
            "MySQL",
          ],
          github: "https://github.com",
          link: "https://google.com",
        },
      ],
    };
  },
};
</script>

<style>
.projects {
  /* height: 100vh; */
  margin-top: 200px;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.projects-list {
  gap: 150px;
}
.project-title {
  margin-bottom: 30px;
}
.project-description {
  width: 500px;
  margin-bottom: 30px;
}
.tech-stack {
  font-size: 20px;
  margin-bottom: 15px;
}
.project-tech-stack {
  width: 500px;
  gap: 10px 20px;
  margin-bottom: 30px;
}
.tech {
  color: var(--green);
  font-size: 18px;
}
.links {
  gap: 20px;
}
.project-image {
  width: 700px;
}
</style>