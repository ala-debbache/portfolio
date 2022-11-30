<template>
  <section class="experience w-full">
    <div class="section-header">
      <h2 class="section-title">Experience</h2>
      <h1 class="section-title-stroke">Experience</h1>
    </div>

    <div class="timeline-section">
      <div class="timeline-items">
        <div v-for="(item, index) in items" :key="index" class="timeline-item">
          <div class="timeline-dot"></div>
          <div class="timeline-date">{{ item.year }}</div>
          <div class="timeline-content">
            <h3>{{ item.title }}</h3>
            <p>{{ item.description }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Experience",
  data() {
    return {
      items: [
        {
          year: "2020",
          title: "Lorem ipsum",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.",
        },
        {
          year: "2022",
          title: "Lorem ipsum",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.",
        },
        {
          year: "2022",
          title: "Lorem ipsum",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.",
        },
      ],
    };
  },
};
</script>

<style>
.experience {
  margin-top: 200px;
}
.timeline-items {
  display: flex;
  flex-wrap: wrap;
  position: relative;
}
.timeline-items::before {
  content: "";
  position: absolute;
  width: 2px;
  height: 100%;
  background-color: var(--dark_blue);
  left: calc(50% - 1px);
}
.timeline-item {
  margin-bottom: 40px;
  width: 100%;
  position: relative;
}
.timeline-item:last-child {
  margin-bottom: 0;
}
.timeline-item:nth-child(odd) {
  padding-right: calc(50% + 30px);
}
.timeline-item:nth-child(even) {
  padding-left: calc(50% + 30px);
}
.timeline-dot {
  height: 16px;
  width: 16px;
  background-color: var(--green);
  position: absolute;
  left: calc(50% - 8px);
  border-radius: 50%;
  top: 10px;
}
.timeline-date {
  font-size: 18px;
  color: var(--green);
  margin: 6px 0 15px;
}
.timeline-content {
  background-color: var(--dark_blue);
  padding: 30px;
  border-radius: 5px;
}
.timeline-content h3 {
  font-size: 22px;
  color: var(--white);
  margin: 0 0 10px;
  text-transform: capitalize;
  font-weight: 500;
}
.timeline-content p {
  color: var(--white);
  font-size: 18px;
}

/* responsive */
@media (max-width: 1024px) {
  .timeline-items::before {
    left: 7px;
  }
  .timeline-item:nth-child(odd) {
    padding-right: 0;
  }
  .timeline-item:nth-child(odd),
  .timeline-item:nth-child(even) {
    padding-left: 37px;
  }
  .timeline-dot {
    left: 0;
  }
}
</style>