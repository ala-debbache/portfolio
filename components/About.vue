<template>
  <section class="about w-full">
    <div class="section-header">
      <h2 class="section-title">About me</h2>
      <h1 class="section-title-stroke">ABOUT</h1>
    </div>
    <div class="content flex justify-between w-full">
      <div class="w-1/2 about-details">
        <p class="description" style="margin-bottom: 20px">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
          minim veniam
        </p>
        <p class="description" style="margin-bottom: 15px">
          Here are a few technologies I’ve been working with recently:
        </p>
        <div class="flex skills">
          <div class="col">
            <ul class="flex flex-col skills-list">
              <li class="flex items-center skill">
                <inline-svg
                  :src="require('@/assets/icons/list-item.svg')"
                  width="12"
                  height="12"
                  aria-label="Item"
                ></inline-svg>
                <span>Javascript</span>
              </li>
              <li class="flex items-center skill">
                <inline-svg
                  :src="require('@/assets/icons/list-item.svg')"
                  width="12"
                  height="12"
                  aria-label="Item"
                ></inline-svg>
                <span>Typescript</span>
              </li>
              <li class="flex items-center skill">
                <inline-svg
                  :src="require('@/assets/icons/list-item.svg')"
                  width="12"
                  height="12"
                  aria-label="Item"
                ></inline-svg>
                <span>Laravel</span>
              </li>
            </ul>
          </div>
          <div class="col">
            <ul class="flex flex-col skills-list">
              <li class="flex items-center skill">
                <inline-svg
                  :src="require('@/assets/icons/list-item.svg')"
                  width="12"
                  height="12"
                  aria-label="Item"
                ></inline-svg>
                <span>Vue JS</span>
              </li>
              <li class="flex items-center skill">
                <inline-svg
                  :src="require('@/assets/icons/list-item.svg')"
                  width="12"
                  height="12"
                  aria-label="Item"
                ></inline-svg>
                <span>Node JS</span>
              </li>
              <li class="flex items-center skill">
                <inline-svg
                  :src="require('@/assets/icons/list-item.svg')"
                  width="12"
                  height="12"
                  aria-label="Item"
                ></inline-svg>
                <span>Electron JS</span>
              </li>
            </ul>
          </div>
        </div>
        <a href="#" target="_blank" class="button-outline">Download my cv</a>
      </div>
      <div class="flex justify-center items-start w-1/2 about-image">
        <img
          src="@/assets/images/my-image.png"
          class="position-relative image"
          alt=""
        />
        <img
          src="@/assets/images/my-image-bg.png"
          class="position-relative bg"
          alt=""
        />
      </div>
    </div>
  </section>
</template>

<script>
import InlineSvg from "vue-inline-svg";
export default {
  name: "About",
  components: {
    InlineSvg,
  },
};
</script>

<style>
.about {
  /* height: 100vh; */
  margin-top: 100px;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.position-relative {
  position: relative;
}
.image {
  z-index: 1;
  width: 300px;
}
.bg {
  margin-left: -265px;
  margin-top: 25px;
  z-index: -1 !important;
}
.skills {
  gap: 150px;
}
.skills-list {
  gap: 15px;
  margin-bottom: 30px;
}
.skill {
  gap: 5px;
}
.skill span {
  font-size: 18px;
}

@media screen and (min-width: 1600px) {
  .image {
    width: 400px;
  }
  .bg {
    height: 400px;
    margin-left: -360px;
    margin-top: 25px;
  }
}

@media screen and (max-width: 1200px) {
  .image {
    width: 250px;
  }
  .bg {
    height: 250px;
    margin-left: -225px;
    margin-top: 25px;
  }
}

@media screen and (max-width: 1150px) {
  .content {
    flex-direction: column;
    gap: 30px;
  }
  .skills {
    gap: 100px;
  }
  .about-details,
  .about-image {
    width: 100%;
  }
  .image {
    width: 300px;
  }
  .bg {
    height: 300px;
    margin-left: -265px;
    margin-top: 25px;
  }
}

@media screen and (max-width: 768px) {
  .footer-links {
    display: flex;
  }
}
</style>