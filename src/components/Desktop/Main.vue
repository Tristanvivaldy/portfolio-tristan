<template>
  <div id="smooth-wrapper" class="overflow-hidden">
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
import Navbar from "./Navbar.vue";
import Hero from "./Hero.vue";
import About from "./About.vue";
import Resume from "./Resume.vue";
import Portfolio from "./Portfolio.vue";
import Contact from "./Contact.vue";

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
</style>