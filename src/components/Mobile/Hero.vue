<template>
  <div class="relative w-full h-full overflow-hidden">
    <div id="hero-bg" class="absolute w-full h-full z-0 duration-300"></div>
    <div
      class="dark:bg-[#222222] bg-[#F0ECE8] text-white px-10 crimson-text-regular py-5 z-10"
    >
      <div
        class="mt-20"
        data-aos="zoom-in"
        data-aos-duration="500"
        data-aos-easing="ease-out"
      >
        <div
          class="dark:bg-[#F4EFED] bg-[#222222] left-1/2 -translate-x-1/2 bottom-1/2 translate-y-1/2 absolute w-8/12 h-11/12 rounded-t-full backdrop-blur-sm opacity-80 shadow-2xl transition-all duration-500 ease-in-out"
        ></div>
        <div class="picture">
          <img
            src="../../assets/hero-picture.png"
            class="relative bottom-15 scale-150"
            alt="hero-picture"
          />
        </div>
      </div>
      <div
        class="p-5"
        data-aos="zoom-in"
        data-aos-duration="500"
        data-aos-easing="ease-out"
      >
        <div
          class="hero-welcome text-center text-xl my-3 dark:text-white text-black"
        >
          Welcome
        </div>
        <div
          class="hero-title text-center text-2xl tracking-wider dark:text-white text-black"
        >
          Hi, I’m
          <span class="dark:text-[#F68CC2] text-[#C14493] duration-200">
            Tristan Vivaldy
          </span>
          a
          <span
            class="dark:text-[#29FF5F] text-[#00B730]"
            ref="typingJobs"
          ></span>
        </div>
        <div class="hero-description my-5 text-lg text-center">
          <div class="hero-subtitle text-black dark:text-white">
            I am a skilled developer with expertise in building full-stack web
            applications, combining interactive front-end development and
            powerful back-end systems.
          </div>
          <div class="flex justify-center items-center">
            <a
              href="/files/Curriculum Vitae - Tristan Vivaldy.pdf"
              download
              class="mt-5 flex px-4 py-2 rounded-xl w-fit cursor-pointer border-1 text-lg hover:dark:bg-[#F68CC2] hover:bg-[#C14493] hover:text-white duration-200 text-black dark:text-white"
            >
              Download CV
            </a>
          </div>
          <div class="hero-connect my-5">
            <div class="connect-title text-black dark:text-white">
              Let’s connect with me.
            </div>
            <div
              class="connect-icons my-4 flex justify-center items-center gap-5"
            >
              <a
                class="dark:text-white text-black hover:dark:text-[#F68CC2] hover:text-[#C14493] hover:scale-125 duration-300"
                href="https://github.com/Tristanvivaldy"
                target="_blank"
                rel="noopener noreferrer"
                ><GithubIcon
              /></a>
              <a
                class="dark:text-white text-black hover:dark:text-[#F68CC2] hover:text-[#C14493] hover:scale-125 duration-300"
                href="https://www.linkedin.com/in/tristan-vivaldy/"
                target="_blank"
                rel="noopener noreferrer"
                ><LinkedinIcon
              /></a>
              <a
                class="dark:text-white text-black hover:dark:text-[#F68CC2] hover:text-[#C14493] hover:scale-125 duration-300"
                href="https://www.instagram.com/tristanviva/"
                target="_blank"
                rel="noopener noreferrer"
                ><InstagramIcon
              /></a>
              <a
                class="dark:text-white text-black hover:dark:text-[#F68CC2] hover:text-[#C14493] hover:scale-125 duration-300"
                href="mailto:vivaldytristan@gmail.com"
                target="_blank"
                rel="noopener noreferrer"
                ><GmailIcon
              /></a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
  
<script>
import Typewriter from "typewriter-effect/dist/core";
import GithubIcon from "../../assets/icons/GithubIcon.vue";
import GmailIcon from "../../assets/icons/GmailIcon.vue";
import InstagramIcon from "../../assets/icons/InstagramIcon.vue";
import LinkedinIcon from "../../assets/icons/LinkedinIcon.vue";

export default {
  name: "HeroSection",
  components: {
    GithubIcon,
    LinkedinIcon,
    InstagramIcon,
    GmailIcon,
  },
  mounted() {
    this.typed();
    this.animate(this.isDark);
    this.observeDarkMode();
  },
  data() {
    return {
      isDark: document.documentElement.classList.contains("dark"),
      vantaEffect: null,
    };
  },
  watch: {
    isDark(newVal) {
      this.animate(newVal);
    },
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
    observeDarkMode() {
      const observer = new MutationObserver(() => {
        const newDark = document.documentElement.classList.contains("dark");
        if (newDark !== this.isDark) {
          this.isDark = newDark;
        }
      });
      observer.observe(document.documentElement, {
        attributes: true,
        attributeFilter: ["class"],
      });
    },
    animate(isDark) {
      if (this.vantaEffect) this.vantaEffect.destroy();
      this.vantaEffect = VANTA.NET({
        el: "#hero-bg",
        mouseControls: false,
        touchControls: true,
        gyroControls: false,
        minHeight: 100.0,
        minWidth: 100.0,
        scale: 1.0,
        scaleMobile: 1.0,
        backgroundColor: isDark ? 0x222222 : 0xf0ece8,
        color: isDark ? 0xffffff : 0x000000,

        points: 7.0,
        maxDistance: 10.0,
        spacing: 12.0,
      });
    },
  },
};
</script>
  
  <style>
</style>