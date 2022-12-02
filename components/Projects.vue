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
          <div class="project-description-details">
            <h3 class="project-title">{{ project.title }}</h3>
            <p class="project-description">
              {{ project.description }}
            </p>
          </div>
          <div class="tech-stack-details">
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
              <a :href="project.github" class="project-link" target="_blanck">
                <inline-svg
                  :src="require('@/assets/icons/github.svg')"
                  width="28"
                  height="28"
                  aria-label="Github"
                ></inline-svg
              ></a>
              <a :href="project.link" class="project-link" target="_blanck">
                <inline-svg
                  :src="require('@/assets/icons/link.svg')"
                  width="28"
                  height="28"
                  aria-label="Link"
                ></inline-svg
              ></a>
            </div>
          </div>
        </div>
        <div class="project-image flex justify-center">
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
  margin-bottom: 30px;
}
.project-image {
  width: 700px;
}

@media screen and (min-width: 1600px) {
  .project-description,
  .project-tech-stack {
    width: 600px;
  }
}

@media screen and (min-width: 1800px) {
  .project-description,
  .project-tech-stack {
    width: 700px;
  }
}

@media screen and (max-width: 1600px) {
  .project {
    flex-direction: column;
    gap: 30px;
  }
  .project-details {
    display: flex;
    justify-content: space-between;
  }
  .project-image {
    width: 100%;
  }
  .project-image img {
    width: 80%;
  }
}

@media screen and (max-width: 1350px) {
  .project-tech-stack {
    width: 400px;
  }
}

@media screen and (max-width: 1200px) {
  .projects {
    margin-top: 150px;
  }
  .projects-list {
    gap: 100px;
  }
  .project-details {
    flex-direction: column;
  }
  .project-description,
  .project-tech-stack {
    width: 80%;
  }
  .project-image img {
    width: 100%;
  }
  .project-link svg {
    width: 24px;
    height: 24px;
  }
}

@media screen and (max-width: 768px) {
  .projects {
    margin-top: 100px;
  }
  .project-description,
  .project-tech-stack {
    width: 100%;
  }
}
</style>