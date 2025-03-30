<template>
  <div class="bg-[#F4EFED] px-25 py-25 crimson-text-regular pb-50">
    <div
      class="title text-end text-2xl tracking-[0.8rem] text-[#F68CC2] crimson-text-bold"
    >
      PORTFOLIO
    </div>
    <!-- <div>
      <div class="flex gap-10">
        <img
          src="https://github-readme-stats.vercel.app/api?username=Tristanvivaldy&show_icons=true&theme=radical"
          alt="GitHub Stats"
          class="w-4/12"
        />
        <img
          src="https://github-readme-stats.vercel.app/api/top-langs/?username=Tristanvivaldy&layout=compact"
          alt="Top Languages"
          class="w-3/12"
        />
      </div>
    </div> -->
  </div>
</template>

<script>
import Axios from "axios";

export default {
  name: "Portfolio",
  data() {
    return {};
  },
  mounted() {
    this.fetchGithubData();
  },
  methods: {
    fetchGithubData() {
      Axios.get(`https://api.github.com/users/Tristanvivaldy`)
        .then((response) => {
          console.log(response);
        })
        .catch((error) => console.error("Error fetching data:", error));
    },
  },
};
</script>

<style>
</style>