<template>
  <div>
    <div class="bg-[#F4EFED] px-5 py-10 crimson-text-regular -mt-10">
      <div
        class="title text-end text-lg tracking-[0.3rem] dark:text-[#F68CC2] text-[#C14493] crimson-text-bold"
      >
        PORTFOLIO
      </div>
      <div class="portfolio-container py-5 mt-5 overflow-x-hidden px-5">
        <div
          class="panel hover:opacity-70 duration-300 rounded-b-4xl w-full shadow-xl my-10 relative"
          data-aos="fade-right"
          data-aos-duration="500"
          data-aos-anchor-placement="top-center"
          data-aos-easing="ease-out"
        >
          <a
            href="https://github.com/Tristanvivaldy/portfolio-tristan"
            target="_blank"
            rel="noopener noreferrer"
            class=""
          >
            <div>
              <img
                src="../../assets/p-portfolio.jpg"
                class="rounded-t-4xl"
                alt="portfolio"
              />
              <div class="p-5">
                <div class="card-content mb-5">
                  <div class="card-title text-xl font-semibold">
                    Portfolio Tristan
                  </div>
                  <div class="card-subtitle text-sm">- 18 March 2025 -</div>
                  <div class="card-desc mt-2 text-xs text-justify">
                    Personal online space designed to showcase skills,
                    experience, and projects in a professional and visually
                    appealing way. This project involves designing and
                    developing a fully responsive and interactive portfolio
                    website that highlights personal or professional
                    achievements.
                  </div>
                </div>
                <div class="flex justify-end absolute right-4 bottom-4">
                  <div
                    class="rounded-full bg-white px-2 py-1 text-sm font-bold group-hover:bg-[#222222] group-hover:text-white"
                  >
                    01
                  </div>
                </div>
              </div>
            </div>
          </a>
        </div>
        <div
          class="panel hover:opacity-70 duration-300 rounded-b-4xl w-full shadow-xl my-10 relative"
          data-aos="fade-left"
          data-aos-duration="500"
          data-aos-anchor-placement="top-center"
          data-aos-easing="ease-out"
        >
          <a
            href="https://github.com/Tristanvivaldy/steamapplicationreview"
            target="_blank"
            rel="noopener noreferrer"
          >
            <div>
              <img
                src="../../assets/p-sentimen.jpg"
                class="rounded-t-4xl"
                alt="sentimen"
              />
              <div class="p-5">
                <div class="card-content mb-5">
                  <div class="card-title text-lg font-semibold">
                    Sentiment Analysis on Steam Apps
                  </div>
                  <div class="card-subtitle text-sm">- 9 January 2025 -</div>
                  <div class="card-desc mt-2 text-xs text-justify">
                    This project involves developing a sentiment analysis
                    website for Steam applications. The website allows users to
                    select a Steam app and analyze its user reviews.
                  </div>
                </div>
                <div class="flex justify-end absolute right-4 bottom-4">
                  <div
                    class="rounded-full bg-white text-sm px-2 py-1 font-bold group-hover:bg-[#755F4C] group-hover:text-white"
                  >
                    02
                  </div>
                </div>
              </div>
            </div>
          </a>
        </div>
        <div
          class="panel hover:opacity-70 duration-300 rounded-b-4xl w-full shadow-xl my-10 pb-8 relative"
          data-aos="zoom-in"
          data-aos-duration="500"
          data-aos-anchor-placement="top-center"
          data-aos-easing="ease-out"
        >
          <a
            href="https://github.com/Tristanvivaldy/librerias"
            target="_blank"
            rel="noopener noreferrer"
          >
            <div>
              <img
                src="../../assets/p-librarias.jpg"
                class="rounded-t-4xl"
                alt="librarias"
              />
              <div class="p-5">
                <div class="card-content">
                  <div class="card-title text-xl font-semibold">
                    Librarias Website
                  </div>
                  <div class="card-subtitle text-sm">- 31 December 2023 -</div>
                  <div class="card-desc mt-2 text-xs">
                    This website is designed to provide comprehensive
                    information about books available in a digital library.
                  </div>
                </div>
                <div class="flex justify-end absolute right-4 bottom-4">
                  <div
                    class="rounded-full bg-white text-sm px-2 py-1 font-bold group-hover:bg-[#CACACA] group-hover:text-black"
                  >
                    03
                  </div>
                </div>
              </div>
            </div>
          </a>
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
    <WavePortfolio class="dark:bg-[#222222] bg-[#F0ECE8]" />
  </div>
</template>

<script>
import Axios from "axios";
import WavePortfolio from "../../assets/wave/WavePortfolio.vue";

export default {
  name: "Portfolio",
  data() {
    return {};
  },
  components: {
    WavePortfolio,
  },
  mounted() {
    // this.fetchGithubData();
  },
  methods: {
    // fetchGithubData() {
    //   Axios.get(`https://api.github.com/users/Tristanvivaldy`)
    //     .then((response) => {
    //       console.log(response);
    //     })
    //     .catch((error) => console.error("Error fetching data:", error));
    // },
  },
};
</script>

<style>
</style>