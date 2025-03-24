<template>
  <div
    class="bg-[#222222] text-white grid grid-cols-12 px-25 py-10 crimson-text-regular"
  >
    <div class="col-span-6 p-5">
      <div class="hero-welcome crimson-text-regular-italic text-2xl my-2">
        Welcome
      </div>
      <div class="hero-title text-6xl tracking-wider leading-20">
        Hi, I’m <span class="text-[#F68CC2]"> Tristan Vivaldy </span> a
        <span class="text-[#29FF5F]"> Web Developer </span>
      </div>
      <div class="hero-description my-7 text-2xl text-justify">
        <div class="hero-subtitle">
          I am a skilled developer with expertise in building full-stack web
          applications, combining interactive front-end development and powerful
          back-end systems.
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
    <div class="col-span-6 relative mt-7">
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
</template>

<script>
import GithubIcon from "../assets/icons/GithubIcon.vue";
import GmailIcon from "../assets/icons/GmailIcon.vue";
import InstagramIcon from "../assets/icons/InstagramIcon.vue";
import LinkedinIcon from "../assets/icons/LinkedinIcon.vue";

export default {
  name: "HeroSection",
  components: {
    GithubIcon,
    LinkedinIcon,
    InstagramIcon,
    GmailIcon,
  },
};
</script>

<style>
</style>