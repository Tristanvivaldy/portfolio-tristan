<template>
  <div>
    <div class="bg-[#F4EFED] py-5 crimson-text-regular -mt-20">
      <div
        class="px-25 title text-end text-2xl tracking-[0.8rem] dark:text-[#F68CC2] text-[#C14493] crimson-text-bold"
      >
        PORTFOLIO
      </div>
      <div
        class="portfolio-container flex px-80 py-10 mt-20 gap-100 overflow-x-hidden"
      >
        <a
          href="https://github.com/Tristanvivaldy/portfolio-tristan"
          target="_blank"
          rel="noopener noreferrer"
          class="panel hover:opacity-70 duration-300 rounded-b-4xl min-w-4xl shadow-xl relative"
        >
          <div>
            <img
              src="../../assets/p-portfolio.jpg"
              class="rounded-t-4xl"
              alt="portfolio"
            />
            <div class="p-5">
              <div class="card-content mb-5">
                <div class="card-title text-2xl font-semibold">
                  Portfolio Tristan
                </div>
                <div class="card-subtitle">- 18 March 2025 -</div>
                <div class="card-desc mt-2 text-lg">
                  Personal online space designed to showcase skills, experience,
                  and projects in a professional and visually appealing way.
                  This project involves designing and developing a fully
                  responsive and interactive portfolio website that highlights
                  personal or professional achievements.
                </div>
              </div>
              <div class="flex justify-end absolute right-5 bottom-5">
                <div
                  class="rounded-full bg-white px-3 py-1 font-bold group-hover:bg-[#222222] group-hover:text-white"
                >
                  01
                </div>
              </div>
            </div>
          </div>
        </a>
        <a
          href="https://github.com/Tristanvivaldy/steamapplicationreview"
          target="_blank"
          rel="noopener noreferrer"
          class="panel hover:opacity-70 duration-300 rounded-b-4xl min-w-4xl shadow-xl relative"
        >
          <div>
            <img
              src="../../assets/p-sentimen.jpg"
              class="rounded-t-4xl"
              alt="sentimen"
            />
            <div class="p-5">
              <div class="card-content mb-5">
                <div class="card-title text-2xl font-semibold">
                  Sentiment Analysis on Steam Apps
                </div>
                <div class="card-subtitle">- 9 January 2025 -</div>
                <div class="card-desc mt-2 text-lg">
                  This project involves developing a sentiment analysis website
                  for Steam applications. The website allows users to select a
                  Steam app and analyze its user reviews.
                </div>
              </div>
              <div class="flex justify-end absolute right-5 bottom-5">
                <div
                  class="rounded-full bg-white px-3 py-1 font-bold group-hover:bg-[#755F4C] group-hover:text-white"
                >
                  02
                </div>
              </div>
            </div>
          </div>
        </a>
        <a
          href="https://github.com/Tristanvivaldy/librerias"
          target="_blank"
          rel="noopener noreferrer"
          class="panel hover:opacity-70 duration-300 rounded-b-4xl min-w-4xl shadow-xl relative"
        >
          <div>
            <img
              src="../../assets/p-librarias.jpg"
              class="rounded-t-4xl h-103"
              alt="librarias"
            />
            <div class="p-5">
              <div class="card-content">
                <div class="card-title text-2xl font-semibold">
                  Librarias Website
                </div>
                <div class="card-subtitle">- 31 December 2023 -</div>
                <div class="card-desc mt-2 text-lg">
                  This website is designed to provide comprehensive information
                  about books available in a digital library.
                </div>
              </div>
              <div class="flex justify-end absolute right-5 bottom-5">
                <div
                  class="rounded-full bg-white px-3 py-1 font-bold group-hover:bg-[#CACACA] group-hover:text-black"
                >
                  03
                </div>
              </div>
            </div>
          </div>
        </a>
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
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
import Axios from "axios";
import WavePortfolio from "../../assets/wave/WavePortfolio.vue";

gsap.registerPlugin(ScrollTrigger);
export default {
  name: "Portfolio",
  data() {
    return {};
  },
  components: {
    WavePortfolio,
  },
  mounted() {
    this.portfolioScroll();
    // this.fetchGithubData();
  },
  methods: {
    portfolioScroll() {
      let sections = gsap.utils.toArray(".panel");
      gsap.to(sections, {
        xPercent: -145 * (sections.length - 1),
        ease: "none",
        scrollTrigger: {
          trigger: ".portfolio-container",
          start: "center center",
          pin: true,
          scrub: 1,
          snap: 1 / (sections.length - 1),
          end: () =>
            "+=" + document.querySelector(".portfolio-container").offsetWidth,
        },
      });
    },
  },
};
// fetchGithubData() {
//   Axios.get(`https://api.github.com/users/Tristanvivaldy`)
//     .then((response) => {
//       console.log(response);
//     })
//     .catch((error) => console.error("Error fetching data:", error));
// },
</script>

<style>
</style>