<template>
  <div>
    <MainPageDesktop v-if="!isMobile" />
    <MainPageMobile v-if="isMobile" />
  </div>
</template>

<script>
import AOS from "aos";
import "aos/dist/aos.css";
import MainPageDesktop from "./components/Desktop/Main.vue";
import MainPageMobile from "./components/Mobile/Main.vue";

export default {
  name: "Main",
  components: {
    MainPageDesktop,
    MainPageMobile,
  },
  data() {
    return {
      isMobile: false,
    };
  },
  methods: {
    handleView() {
      this.isMobile = window.innerWidth <= 990;
    },
  },
  beforeMount() {
    this.handleView();
  },
  beforeUnmount() {
    window.removeEventListener("resize", this.handleView);
  },
  mounted() {
    AOS.init();

    window.addEventListener("resize", this.handleView);

    document.querySelectorAll('a[href^="#"]').forEach((anchor) => {
      anchor.addEventListener("click", function (e) {
        e.preventDefault();
        const targetId = this.getAttribute("href").substring(1);
        const targetElement = document.getElementById(targetId);

        if (targetElement) {
          targetElement.scrollIntoView({
            behavior: "smooth",
            block: "start",
          });
        }
      });
    });
  },
};
</script>

<style>
html,
body {
  scroll-behavior: smooth;
}
.rubik-wet-paint {
  font-family: "Rubik Wet Paint", system-ui;
  font-weight: 400;
  font-style: normal;
}
.crimson-text-regular {
  font-family: "Crimson Text", serif;
  font-weight: 400;
  font-style: normal;
}

.crimson-text-semibold {
  font-family: "Crimson Text", serif;
  font-weight: 600;
  font-style: normal;
}

.crimson-text-bold {
  font-family: "Crimson Text", serif;
  font-weight: 700;
  font-style: normal;
}

.crimson-text-regular-italic {
  font-family: "Crimson Text", serif;
  font-weight: 400;
  font-style: italic;
}

.crimson-text-semibold-italic {
  font-family: "Crimson Text", serif;
  font-weight: 600;
  font-style: italic;
}

.crimson-text-bold-italic {
  font-family: "Crimson Text", serif;
  font-weight: 700;
  font-style: italic;
}
</style>