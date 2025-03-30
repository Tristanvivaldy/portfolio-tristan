<template>
  <div class="navbar">
    <Navbar />
  </div>
  <div class="content">
    <div class="hero">
      <Hero />
    </div>
    <div class="about">
      <About />
    </div>
    <div class="resume">
      <Resume />
    </div>
    <div class="portfolio">
      <Portfolio />
    </div>
    <div class="contact">
      <Contact />
    </div>
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
};
</script>

<style>
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