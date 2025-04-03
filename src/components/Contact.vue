<template>
  <div
    class="bg-[#222222] text-white px-25 crimson-text-regular relative min-h-screen"
  >
    <div
      class="title text-2xl tracking-[0.8rem] text-[#F68CC2] crimson-text-bold"
    >
      CONTACT
    </div>
    <div class="mt-30">
      <div
        class="absolute left-0 bg-white w-5/12 h-[60vh] rounded-r-4xl shadow-xs shadow-white"
        data-aos="fade-right"
        data-aos-duration="750"
        data-aos-anchor-placement="top-center"
      >
        <div class="profile text-black px-10 py-7">
          <p class="font-bold text-[#3E1F92] text-lg">Contact Me</p>
          <p class="font-bold text-3xl">Get In Touch With Me</p>
          <p class="mt-4">
            Fresh Graduate from Maranatha Christian University, majoring in
            Informatics Engineering. I have good problem solving and teamwork
            skills. I am also interested in Data Engineering, Full Stack
            Development, and Mobile Development.
          </p>
          <div class="mt-8">
            <div class="flex gap-2 mt-5 items-center">
              <div><LocationIcon :width="40" :height="40" /></div>
              <div>Bekasi, Indonesia</div>
            </div>
            <div class="flex gap-2 mt-5 items-center">
              <div><EnvelopeIcon :width="40" :height="40" /></div>
              <div>vivaldytristan@gmail.com</div>
            </div>
            <div class="flex gap-2 mt-5 items-center">
              <div><PhoneIcon :width="40" :height="40" /></div>
              <div>+62895338302300</div>
            </div>
          </div>
        </div>
      </div>
      <div
        class="absolute right-0 bg-white w-5/12 h-[60vh] rounded-l-4xl shadow-xs shadow-white"
        data-aos="fade-left"
        data-aos-duration="750"
        data-aos-anchor-placement="top-center"
      >
        <div class="profile text-black px-10 py-7">
          <div class="grid grid-cols-12 gap-10">
            <div class="col-span-6">
              <label class="text-lg font-semibold" for="name">Name</label>
              <input
                type="text"
                id="name"
                class="border-2 mt-2 border-gray-300 rounded-lg p-2 w-full"
                placeholder="Full name"
              />
            </div>
            <div class="col-span-6">
              <label class="text-lg font-semibold" for="email">Email</label>
              <input
                type="email"
                id="email"
                class="border-2 mt-2 border-gray-300 rounded-lg p-2 w-full"
                placeholder="Email Address"
              />
            </div>
          </div>
          <div class="mt-2">
            <label class="text-lg font-semibold" for="phone-number"
              >Phone Number</label
            >
            <input
              type="number"
              id="phone-number"
              class="border-2 mt-2 border-gray-300 rounded-lg p-2 w-full"
              placeholder="Phone Number"
            />
          </div>
          <div class="mt-2">
            <label class="text-lg font-semibold" for="message">Message</label>
            <textarea
              id="message"
              class="border-2 mt-2 border-gray-300 rounded-lg p-2 w-full h-30 resize-none"
              placeholder="Your Message Here..."
            />
          </div>
          <button
            class="mt-1 cursor-pointer px-6 py-2 bg-[#222222] rounded-xl text-white hover:bg-[#424242] duration-200"
            type="submit"
          >
            Submit
          </button>
        </div>
      </div>
    </div>
    <div
      class="absolute left-0 bottom-10 w-full flex justify-center items-center text-xl crimson-text-regular-italic"
      data-aos="zoom-out"
    >
      "Every great project starts with a single commit."
    </div>
  </div>
</template>

<script>
import LocationIcon from "../assets/icons/LocationIcon.vue";
import EnvelopeIcon from "../assets/icons/EnvelopeIcon.vue";
import PhoneIcon from "../assets/icons/PhoneIcon.vue";
export default {
  name: "ContactSection",
  components: {
    LocationIcon,
    EnvelopeIcon,
    PhoneIcon,
  },
};
</script>

<style scoped>
input[type="number"] {
  -appearance: textfield;
}

input[type="number"]::-webkit-inner-spin-button,
input[type="number"]::-webkit-outer-spin-button {
  -webkit-appearance: none;
  margin: 0;
}
</style>