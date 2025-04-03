<template>
  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320">
    <path
      :fill="fill"
      fill-opacity="1"
      d="M0,64L60,69.3C120,75,240,85,360,80C480,75,600,53,720,37.3C840,21,960,11,1080,37.3C1200,64,1320,128,1380,160L1440,192L1440,0L1380,0C1320,0,1200,0,1080,0C960,0,840,0,720,0C600,0,480,0,360,0C240,0,120,0,60,0L0,0Z"
    ></path>
  </svg>
</template>

<script>
export default {
  name: "WaveSVGPortfolio",
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