<template>
  <nav class="bg-[#222222] text-white flex px-20 py-10 rubik-wet-paint">
    <div class="grid grid-cols-12 gap-4 items-center w-full">
      <div class="col-span-2">Portfolio Website</div>
      <div class="menu col-span-9 flex gap-5 justify-end">
        <a href="#" class="text-sm hover:text-gray-400">HOME</a>
        <a href="#" class="text-sm hover:text-gray-400">ABOUT</a>
        <a href="#" class="text-sm hover:text-gray-400">RESUME</a>
        <a href="#" class="text-sm hover:text-gray-400">PORTFOLIO</a>
        <a href="#" class="text-sm hover:text-gray-400">CONTACT</a>
      </div>
      <div class="col-span-1">
        <button class="border-2 w-fit rounded-full p-1">
          <DarkmodeIcon :width="25" :height="25" class="block" />
          <LightmodeIcon :width="25" :height="25" class="hidden" />
        </button>
      </div>
    </div>
  </nav>
</template>

<script>
import DarkmodeIcon from "../assets/icons/DarkModeIcon.vue";
import LightmodeIcon from "../assets/icons/LightModeIcon.vue";
export default {
  name: "Navbar",
  components: {
    DarkmodeIcon,
    LightmodeIcon,
  },
};
</script>

<style>
</style>