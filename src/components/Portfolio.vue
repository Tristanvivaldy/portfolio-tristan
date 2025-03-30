<template>
  <div class="bg-[#F4EFED] px-25 py-25 crimson-text-regular pb-50">
    <div
      class="title text-end text-2xl tracking-[0.8rem] text-[#F68CC2] crimson-text-bold"
    >
      PORTFOLIO
    </div>
    <div class="container flex mt-20 gap-5">
      <div
        class="group flex items-center justify-center bg-[#222222] w-20 h-100 shadow rounded-4xl hover:duration-400 hover:w-100 hover:items-start hover:justify-start hover:bg-white relative"
      >
        <div
          class="content-show [writing-mode:vertical-rl] text-white font-extralight group-hover:hidden group-hover:duration-200"
        >
          Portfolio Tristan
        </div>
        <div class="content-show hidden group-hover:block">
          <img
            src="../assets/p-portfolio.jpg"
            class="rounded-t-4xl duration-500 hover:scale-110 hover:opacity-80 shadow-xl"
            alt="portfolio"
          />
          <div class="card-content py-5 px-5">
            <div class="card-title text-2xl font-semibold">
              Portfolio Tristan
            </div>
            <div class="card-subtitle">- 18 March 2025 -</div>
            <div class="card-desc mt-2 text-sm">
              Personal online space designed to showcase skills, experience, and
              projects in a professional and visually appealing way.
            </div>
            <button
              class="absolute left-5 bottom-5 px-4 py-2 bg-[#222222] text-white rounded-2xl cursor-pointer hover:opacity-70 hover:duration-200"
            >
              Click Me!
            </button>
          </div>
        </div>
        <div class="flex justify-end absolute bottom-5 right-5">
          <div
            class="rounded-full bg-white px-3 py-1 font-bold group-hover:bg-[#222222] group-hover:text-white"
          >
            01
          </div>
        </div>
      </div>
      <div
        class="group flex items-center justify-center bg-[#755F4C] w-20 h-100 shadow rounded-4xl hover:duration-400 hover:w-100 hover:items-start hover:justify-start hover:bg-white relative"
      >
        <div
          class="content-show [writing-mode:vertical-rl] text-white font-extralight group-hover:hidden group-hover:duration-200"
        >
          Sentiment Analysis
        </div>
        <div class="content-show hidden group-hover:block">
          <img
            src="../assets/p-sentimen.jpg"
            class="rounded-t-4xl duration-500 hover:scale-110 hover:opacity-80 shadow-xl"
            alt="sentimen"
          />
          <div class="card-content py-5 px-5">
            <div class="card-title text-2xl font-semibold">
              Sentiment Analysis on Steam Apps
            </div>
            <div class="card-subtitle">- 9 January 2025 -</div>
            <div class="card-desc mt-2 text-sm">
              This project involves developing a sentiment analysis website for
              Steam applications. The website allows users to select a Steam app
              and analyze its user reviews.
            </div>
            <button
              class="absolute left-5 bottom-5 px-4 py-2 bg-[#755F4C] text-white rounded-2xl cursor-pointer hover:opacity-70 hover:duration-200"
            >
              Click Me!
            </button>
          </div>
        </div>
        <div class="flex justify-end absolute bottom-5 right-5">
          <div
            class="rounded-full bg-white px-3 py-1 font-bold group-hover:bg-[#755F4C] group-hover:text-white"
          >
            02
          </div>
        </div>
      </div>
      <div
        class="group flex items-center justify-center bg-[#CACACA] w-20 h-100 shadow rounded-4xl hover:duration-400 hover:w-100 hover:items-start hover:justify-start hover:bg-white relative"
      >
        <div
          class="content-show [writing-mode:vertical-rl] text-black font-extralight group-hover:hidden group-hover:duration-200"
        >
          Librarias
        </div>
        <div class="content-show hidden group-hover:block">
          <img
            src="../assets/p-librarias.jpg"
            class="rounded-t-4xl duration-500 hover:scale-110 hover:opacity-80 shadow-xl"
            alt="librarias"
          />
          <div class="card-content py-5 px-5">
            <div class="card-title text-2xl font-semibold">
              Librarias Website
            </div>
            <div class="card-subtitle">- 31 December 2023 -</div>
            <div class="card-desc mt-2 text-sm">
              This website is designed to provide comprehensive information
              about books available in a digital library.
            </div>
            <button
              class="absolute left-5 bottom-5 px-4 py-2 bg-[#CACACA] text-black rounded-2xl cursor-pointer hover:opacity-70 hover:duration-200"
            >
              Click Me!
            </button>
          </div>
        </div>
        <div class="flex justify-end absolute bottom-5 right-5">
          <div
            class="rounded-full bg-white px-3 py-1 font-bold group-hover:bg-[#CACACA] group-hover:text-black"
          >
            03
          </div>
        </div>
      </div>
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