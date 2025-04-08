<template>
  <div>
    <div class="bg-[#F4EFED] px-5 crimson-text-regular py-10">
      <div
        class="title text-end text-lg tracking-[0.3rem] dark:text-[#F68CC2] text-[#C14493] crimson-text-bold"
      >
        ABOUT
      </div>
      <div class="section-about-me text-center">
        <div class="crimson-text-bold text-3xl my-7">What I Do</div>
        <div class="px-10">
          <div class="flex justify-center items-center" data-aos="fade-right">
            <img src="../../assets/what-i-do-vector.png" alt="what-i-do" />
          </div>
          <div
            class="description-about-me mt-5 text-lg text-start"
            data-aos="fade-left"
          >
            I create clean, modern, and user-friendly websites that deliver
            great online experiences. What does that mean? Three things: <br />
            <br />
            <b> 1. Technical - </b> Well-structured code, optimized for
            performance, fast loading, and built with best practices in mind.
            <br />
            <b> 2. Design - </b> Thoughtful design with balanced layouts,
            ensuring a polished and professional look. <br />
            <b> 3. User-Friendly - </b> Intuitive and accessible, making it easy
            for anyone to navigate and interact. <br /><br />
            As a fresh graduate, I’m eager to apply my skills and continuously
            learn to build even better digital solutions.
          </div>
        </div>
      </div>
      <div class="section-skills text-center">
        <div class="crimson-text-bold text-3xl mt-15 mb-10">Skills</div>
        <div
          class="skills-logo flex overflow-hidden relative"
          data-aos="zoom-in"
          data-aos-duration="500"
        >
          <div class="flex gap-10 logo-track">
            <img
              src="../../assets/skills-logo/html.png"
              class="h-12 hover:animate-none"
              alt="html"
            />
            <img
              src="../../assets/skills-logo/css.png"
              class="h-12"
              alt="css"
            />
            <img
              src="../../assets/skills-logo/vue.png"
              class="h-12"
              alt="vue"
            />
            <img
              src="../../assets/skills-logo/php.png"
              class="h-12"
              alt="php"
            />
            <img src="../../assets/skills-logo/go.png" class="h-12" alt="go" />
            <img src="../../assets/skills-logo/py.png" class="h-12" alt="py" />
            <img
              src="../../assets/skills-logo/pgsql.png"
              class="h-12"
              alt="pgsql"
            />
            <img
              src="../../assets/skills-logo/tailwind.png"
              class="w-10"
              alt="tailwind"
            />

            <img
              src="../../assets/skills-logo/html.png"
              class="h-12"
              alt="html"
            />
            <img
              src="../../assets/skills-logo/css.png"
              class="h-12"
              alt="css"
            />
            <img
              src="../../assets/skills-logo/vue.png"
              class="h-12"
              alt="vue"
            />
            <img
              src="../../assets/skills-logo/php.png"
              class="h-12"
              alt="php"
            />
            <img src="../../assets/skills-logo/go.png" class="h-12" alt="go" />
            <img src="../../assets/skills-logo/py.png" class="h-12" alt="py" />
            <img
              src="../../assets/skills-logo/pgsql.png"
              class="h-12"
              alt="pgsql"
            />
            <img
              src="../../assets/skills-logo/tailwind.png"
              class="w-10"
              alt="tailwind"
            />
          </div>
          <div
            class="absolute pointer-events-none z-10 left-0 top-0 h-full w-20 bg-gradient-to-r from-[#F4EFED] to-transparent"
          ></div>
          <div
            class="absolute pointer-events-none z-10 right-0 top-0 h-full w-20 bg-gradient-to-l from-[#F4EFED] to-transparent"
          ></div>
        </div>
      </div>
    </div>
    <WaveAbout class="dark:bg-[#222222] bg-[#F0ECE8]" />
  </div>
</template>
  
  <script>
import WaveAbout from "../../assets/wave/WaveAbout.vue";

export default {
  name: "AboutSection",
  components: {
    WaveAbout,
  },
};
</script>
  
  <style>
.skills-logo {
  width: 100%;
  white-space: nowrap;
}
.logo-track {
  animation: marquee 5s linear infinite;
  width: max-content;
}

@keyframes marquee {
  from {
    transform: translateX(0%);
  }
  to {
    transform: translateX(-120%);
  }
}
</style>