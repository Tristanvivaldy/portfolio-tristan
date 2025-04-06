<template>
  <nav
    class="dark:bg-[#222222] bg-[#F0ECE8] text-white flex px-20 py-10 rubik-wet-paint"
  >
    <div class="grid grid-cols-12 gap-4 items-center w-full">
      <div class="col-span-2 duration-200 dark:text-white text-black">
        Portfolio Website
      </div>

      <div
        class="menu col-span-9 flex gap-5 justify-end dark:text-white text-black"
      >
        <a
          href="#home"
          class="text-sm dark:hover:text-gray-400 duration-200 hover:text-gray-600"
          >HOME</a
        >
        <a
          href="#about"
          class="text-sm dark:hover:text-gray-400 duration-200 hover:text-gray-600"
          >ABOUT</a
        >
        <a
          href="#resume"
          class="text-sm dark:hover:text-gray-400 duration-200 hover:text-gray-600"
          >RESUME</a
        >
        <a
          href="#portfolio"
          class="text-sm dark:hover:text-gray-400 duration-200 hover:text-gray-600"
          >PORTFOLIO</a
        >
        <a
          href="#contact"
          class="text-sm dark:hover:text-gray-400 duration-200 hover:text-gray-600"
          >CONTACT</a
        >
      </div>
      <div class="col-span-1">
        <button
          class="ml-5 w-fit rounded-full p-1 duration-200 cursor-pointer hover:scale-150 scale-125"
        >
          <transition name="icon-zoom" mode="out-in">
            <component
              :is="isDark ? 'DarkmodeIcon' : 'LightmodeIcon'"
              :key="isDark"
              :width="25"
              :height="25"
              class="cursor-pointer"
              @click="toggleDarkMode"
            />
          </transition>
        </button>
      </div>
    </div>
  </nav>
</template>

<script>
import DarkmodeIcon from "../../assets/icons/DarkModeIcon.vue";
import LightmodeIcon from "../../assets/icons/LightModeIcon.vue";
export default {
  name: "Navbar",
  components: {
    DarkmodeIcon,
    LightmodeIcon,
  },
  data() {
    return {
      isDark: true,
    };
  },
  methods: {
    toggleDarkMode() {
      this.isDark = !this.isDark;
      const html = document.documentElement;
      if (this.isDark) {
        html.classList.add("dark");
      } else {
        html.classList.remove("dark");
      }
    },
  },
};
</script>

<style scoped>
.icon-zoom-enter-active {
  animation: zoomIn 0.3s ease-out;
}
.icon-zoom-leave-active {
  animation: zoomOut 0.3s ease-in;
}

@keyframes zoomIn {
  from {
    opacity: 0;
    transform: scale(0.6);
  }
  to {
    opacity: 1;
    transform: scale(1);
  }
}

@keyframes zoomOut {
  from {
    opacity: 1;
    transform: scale(1);
  }
  to {
    opacity: 0;
    transform: scale(0.6);
  }
}
</style>