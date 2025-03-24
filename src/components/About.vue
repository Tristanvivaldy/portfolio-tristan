<template>
  <div class="bg-[#F4EFED] px-25 py-25 crimson-text-regular">
    <div
      class="title text-end text-2xl tracking-[0.8rem] text-[#F68CC2] crimson-text-bold"
    >
      ABOUT
    </div>
    <div class="section-about-me text-center">
      <div class="crimson-text-bold text-4xl mt-15 mb-20">What I Do</div>
      <div class="grid grid-cols-12 pl-10">
        <div class="col-span-4 flex justify-center items-center">
          <img
            src="../assets/what-i-do-vector.png"
            alt="what-i-do"
            class="scale-125"
          />
        </div>
        <div class="description-about-me px-50 text-xl text-start col-span-8">
          I create clean, modern, and user-friendly websites that deliver great
          online experiences. What does that mean? Three things: <br />
          <br />
          <b> 1. Technical - </b> Well-structured code, optimized for
          performance, fast loading, and built with best practices in mind.
          <br />
          <b> 2. Design - </b> Thoughtful design with balanced layouts, ensuring
          a polished and professional look. <br />
          <b> 3. User-Friendly - </b> Intuitive and accessible, making it easy
          for anyone to navigate and interact. <br /><br />
          As a fresh graduate, I’m eager to apply my skills and continuously
          learn to build even better digital solutions.
        </div>
      </div>
    </div>
    <div class="section-skills text-center">
      <div class="crimson-text-bold text-4xl mt-30 mb-20">Skills</div>
      <div class="skills-logo flex overflow-hidden relative">
        <div class="flex gap-25 logo-track">
          <img
            src="../assets/skills-logo/html.png"
            class="h-24 hover:animate-none"
            alt="html"
          />
          <img src="../assets/skills-logo/css.png" class="h-24" alt="css" />
          <img src="../assets/skills-logo/vue.png" class="h-24" alt="vue" />
          <img src="../assets/skills-logo/php.png" class="h-24" alt="php" />
          <img src="../assets/skills-logo/go.png" class="h-24" alt="go" />
          <img src="../assets/skills-logo/py.png" class="h-24" alt="py" />
          <img src="../assets/skills-logo/pgsql.png" class="h-24" alt="pgsql" />
          <img
            src="../assets/skills-logo/tailwind.png"
            class="w-20"
            alt="tailwind"
          />

          <img src="../assets/skills-logo/html.png" class="h-24" alt="html" />
          <img src="../assets/skills-logo/css.png" class="h-24" alt="css" />
          <img src="../assets/skills-logo/vue.png" class="h-24" alt="vue" />
          <img src="../assets/skills-logo/php.png" class="h-24" alt="php" />
          <img src="../assets/skills-logo/go.png" class="h-24" alt="go" />
          <img src="../assets/skills-logo/py.png" class="h-24" alt="py" />
          <img src="../assets/skills-logo/pgsql.png" class="h-24" alt="pgsql" />
          <img
            src="../assets/skills-logo/tailwind.png"
            class="w-20"
            alt="tailwind"
          />
        </div>
        <div
          class="absolute left-0 top-0 h-full w-50 bg-gradient-to-r from-[#F4EFED] to-transparent"
        ></div>
        <div
          class="absolute right-0 top-0 h-full w-50 bg-gradient-to-l from-[#F4EFED] to-transparent"
        ></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AboutSection",
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
    transform: translateX(-107%);
  }
}
</style>