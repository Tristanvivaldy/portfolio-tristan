<template>
  <div class="relative w-full h-full">
    <div id="hero-bg" class="absolute w-full h-full"></div>
    <div
      class="bg-[#222222] text-white grid grid-cols-12 px-25 crimson-text-regular py-10 z-10"
    >
      <div
        class="col-span-6 p-5"
        data-aos="fade-right"
        data-aos-duration="1000"
        data-aos-easing="ease-out"
      >
        <div class="hero-welcome text-2xl my-2">Welcome.</div>
        <div class="hero-title text-6xl tracking-wider leading-20">
          Hi, I’m <span class="text-[#F68CC2]"> Tristan Vivaldy </span> a
          <span class="text-[#29FF5F]" ref="typingJobs"></span>
        </div>
        <div class="hero-description my-7 text-2xl text-justify">
          <div class="hero-subtitle">
            I am a skilled developer with expertise in building full-stack web
            applications, combining interactive front-end development and
            powerful back-end systems.
          </div>
          <div class="hero-connect my-7">
            <div class="connect-title">Let’s connect with me.</div>
            <div class="connect-icons my-4 flex gap-4">
              <a href=""><GithubIcon /></a>
              <a href=""><LinkedinIcon /></a>
              <a href=""><InstagramIcon /></a>
              <a href=""><GmailIcon /></a>
            </div>
          </div>
        </div>
      </div>
      <div
        class="col-span-6 relative mt-7"
        data-aos="fade-left"
        data-aos-duration="1000"
        data-aos-easing="ease-out"
      >
        <div
          class="shape-2 bg-[#F4EFED] left-2/8 bottom-5/27 absolute w-6/12 h-8/12 rounded-t-full"
        ></div>
        <div class="picture">
          <img
            src="../assets/hero-picture.png"
            class="absolute bottom-5/22 scale-110"
            alt="hero-picture"
          />
        </div>
      </div>
    </div>
    <WaveHero class="bg-[#F4EFED] relative" />
  </div>
</template>

<script>
import Typewriter from "typewriter-effect/dist/core";
import GithubIcon from "../assets/icons/GithubIcon.vue";
import GmailIcon from "../assets/icons/GmailIcon.vue";
import InstagramIcon from "../assets/icons/InstagramIcon.vue";
import LinkedinIcon from "../assets/icons/LinkedinIcon.vue";
import WaveHero from "../assets/wave/WaveHero.vue";

export default {
  name: "HeroSection",
  components: {
    GithubIcon,
    LinkedinIcon,
    InstagramIcon,
    GmailIcon,
    WaveHero,
  },
  mounted() {
    this.typed();
    VANTA.NET({
      el: "#hero-bg",
      mouseControls: true,
      touchControls: true,
      gyroControls: false,
      minHeight: 200.0,
      minWidth: 200.0,
      scale: 1,
      scaleMobile: 1.0,
      backgroundColor: 0x222222,
      color: 0xffffff,
      points: 7.0,
      maxDistance: 20.0,
      spacing: 18.0,
    });
  },
  methods: {
    typed() {
      const typingJobs = this.$refs.typingJobs;

      if (!typingJobs) return;

      new Typewriter(typingJobs, {
        loop: true,
        delay: 100,
      })
        .typeString("Web Developer.")
        .pauseFor(1000)
        .deleteAll()
        .typeString("Fullstack Developer.")
        .pauseFor(1000)
        .start();
    },
  },
};
</script>

<style>
</style>