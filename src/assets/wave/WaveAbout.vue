<template>
  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1435 320">
    <path
      :fill="fill"
      fill-opacity="1"
      d="M0,64L80,96C160,128,320,192,480,181.3C640,171,800,85,960,64C1120,43,1280,85,1360,106.7L1440,128L1440,0L1360,0C1280,0,1120,0,960,0C800,0,640,0,480,0C320,0,160,0,80,0L0,0Z"
    ></path>
  </svg>
</template>

<script>
export default {
  name: "WaveSVGAbout",
  props: {
    fill: {
      type: String,
      default: "#F4EFED",
    },
  },
};
</script>

<style>
</style>