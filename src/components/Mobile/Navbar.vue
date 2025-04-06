<template>
  <nav class="bg-[#F0ECE8] dark:bg-[#222222] px-4 py-3 shadow-md md:hidden">
    <div class="flex items-center justify-between">
      <button
        @click="isOpen = !isOpen"
        class="text-gray-800 dark:text-white focus:outline-none"
      >
        <DropdownLogo :isOpen="isOpen" />
      </button>
      <div class="text-xl font-semibold text-black dark:text-white">
        Portfolio.
      </div>
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
    <transition name="fade">
      <div
        v-if="isOpen"
        class="absolute top-13 left-0 w-full bg-[#F0ECE8] dark:bg-[#222222] text-black dark:text-white px-6 py-4 flex flex-col gap-3 z-50 shadow-lg"
      >
        <a
          href="#home"
          class="dark:hover:text-gray-400 duration-200 hover:text-gray-600"
          @click="closeMenu"
          >HOME</a
        >
        <a
          href="#about"
          class="dark:hover:text-gray-400 duration-200 hover:text-gray-600"
          @click="closeMenu"
          >ABOUT</a
        >
        <a
          href="#resume"
          class="dark:hover:text-gray-400 duration-200 hover:text-gray-600"
          @click="closeMenu"
          >RESUME</a
        >
        <a
          href="#portfolio"
          class="dark:hover:text-gray-400 duration-200 hover:text-gray-600"
          @click="closeMenu"
          >PORTFOLIO</a
        >
        <a
          href="#contact"
          class="dark:hover:text-gray-400 duration-200 hover:text-gray-600"
          @click="closeMenu"
          >CONTACT</a
        >
      </div>
    </transition>
  </nav>
</template>
  
<script>
import DropdownLogo from "../../assets/icons/DropdownLogo.vue";

import DarkmodeIcon from "../../assets/icons/DarkModeIcon.vue";
import LightmodeIcon from "../../assets/icons/LightModeIcon.vue";
export default {
  name: "Navbar",
  components: {
    DropdownLogo,
    DarkmodeIcon,
    LightmodeIcon,
  },
  data() {
    return {
      isOpen: false,
      isDark: true,
    };
  },
  methods: {
    toggleMenu() {
      this.isOpen = !this.isOpen;
    },
    closeMenu() {
      this.isOpen = false;
    },
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