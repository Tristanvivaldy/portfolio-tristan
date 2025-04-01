<template>
  <div id="smooth-wrapper">
    <section class="navbar">
      <Navbar />
    </section>
    <section class="content">
      <section id="hero" class="hero">
        <Hero />
      </section>
      <section id="about" class="about">
        <About />
      </section>
      <section id="resume" class="resume">
        <Resume />
      </section>
      <section id="portfolio" class="portfolio">
        <Portfolio />
      </section>
      <section id="contact" class="contact">
        <Contact />
      </section>
    </section>
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import Hero from "./components/Hero.vue";
import About from "./components/About.vue";
import Resume from "./components/Resume.vue";
import Portfolio from "./components/Portfolio.vue";
import Contact from "./components/Contact.vue";

export default {
  name: "Home",
  components: {
    Navbar,
    Hero,
    About,
    Resume,
    Portfolio,
    Contact,
  },
  mounted() {},
  methods: {},
};
</script>

<style>
.smooth-wrapper {
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