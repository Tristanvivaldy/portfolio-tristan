<template>
  <div
    class="dark:bg-[#222222] bg-[#F0ECE8] text-white px-5 pt-10 crimson-text-regular relative min-h-screen -mt-8"
  >
    <div
      class="title text-lg tracking-[0.3rem] dark:text-[#F68CC2] text-[#C14493] crimson-text-bold"
    >
      CONTACT
    </div>
    <div class="mt-10">
      <div
        class="relative left-1/2 px-6 py-4 my-10 -translate-x-1/2 bg-white w-10/12 rounded-xl shadow-xs shadow-white"
        data-aos="fade-right"
        data-aos-duration="500"
        data-aos-anchor-placement="top-center"
      >
        <div class="profile text-black px-5 py-4">
          <p class="font-bold text-[#3E1F92] text-xl">Contact Me</p>
          <p class="font-bold text-2xl">Get In Touch With Me</p>
          <p class="mt-2 text-md">
            Fresh Graduate from Maranatha Christian University, majoring in
            Informatics Engineering. I have good problem solving and teamwork
            skills. I am also interested in Data Engineering, Full Stack
            Development, and Mobile Development.
          </p>
          <div class="mt-2">
            <div class="flex gap-2 mt-5 items-center">
              <div><LocationIcon :width="20" :height="20" /></div>
              <div>Bekasi, Indonesia</div>
            </div>
            <div class="flex gap-2 mt-5 items-center">
              <div><EnvelopeIcon :width="20" :height="20" /></div>
              <div>vivaldytristan@gmail.com</div>
            </div>
            <div class="flex gap-2 mt-5 items-center">
              <div><PhoneIcon :width="20" :height="20" /></div>
              <div>+62895338302300</div>
            </div>
          </div>
        </div>
      </div>
      <div
        class="relative left-1/2 px-6 py-4 my-10 -translate-x-1/2 bg-white w-10/12 rounded-xl shadow-xs shadow-white"
        data-aos="fade-left"
        data-aos-duration="500"
        data-aos-anchor-placement="top-center"
      >
        <form @submit.prevent="submitForm" class="profile text-black px-2 py-1">
          <div class="mt-2">
            <label class="text-sm font-semibold" for="name">Full Name</label>
            <input
              v-model="userName"
              type="text"
              class="border-2 mt-2 border-gray-300 rounded-lg p-2 w-full"
              placeholder="Full name"
              required
            />
          </div>
          <div class="mt-2">
            <label class="text-sm font-semibold" for="email"
              >Email Address</label
            >
            <input
              v-model="userEmail"
              type="email"
              class="border-2 mt-2 border-gray-300 rounded-lg p-2 w-full"
              placeholder="Email"
              required
            />
          </div>
          <div class="mt-2">
            <label class="text-sm font-semibold" for="phone-number"
              >Phone Number</label
            >
            <input
              v-model="userPhone"
              type="number"
              class="border-2 mt-2 border-gray-300 rounded-lg p-2 w-full"
              placeholder="Phone Number"
              required
            />
          </div>
          <div class="mt-2">
            <label class="text-sm font-semibold" for="message">Message</label>
            <textarea
              v-model="userMessage"
              class="border-2 mt-2 border-gray-300 rounded-lg p-2 w-full h-30 resize-none"
              placeholder="Your Message Here..."
              required
            />
          </div>
          <button
            class="mt-2 cursor-pointer px-6 py-2 bg-[#222222] rounded-xl text-white hover:bg-[#424242] duration-200"
            type="submit"
            @click="sentMessage"
          >
            Submit
          </button>
        </form>
      </div>
    </div>
    <div
      class="relative bottom-5 py-5 w-full flex justify-center items-center text-lg crimson-text-regular-italic text-black dark:text-white"
      data-aos="zoom-out"
      data-aos-anchor-placement="top-bottom"
    >
      "Every great project starts with a single commit."
    </div>
  </div>
</template>

<script>
import LocationIcon from "../../assets/icons/LocationIcon.vue";
import EnvelopeIcon from "../../assets/icons/EnvelopeIcon.vue";
import PhoneIcon from "../../assets/icons/PhoneIcon.vue";
import { useToast } from "vue-toastification";
export default {
  name: "ContactSection",
  components: {
    LocationIcon,
    EnvelopeIcon,
    PhoneIcon,
  },
  data() {
    return {
      userName: "",
      userEmail: "",
      userPhone: "",
      userMessage: "",
    };
  },
  methods: {
    sentMessage() {
      const toast = useToast();
      const formData = new FormData();
      formData.append("entry.1953570482", this.userName);
      formData.append("entry.816137974", this.userEmail);
      formData.append("entry.603370130", this.userPhone);
      formData.append("entry.14687467", this.userMessage);

      fetch(
        "https://docs.google.com/forms/d/e/1FAIpQLScbRpZFz39hU7LNHni1ftvETd_D-ugwrLHTq5H5hvzOPHK_ug/formResponse",
        {
          method: "POST",
          body: formData,
          mode: "no-cors",
        }
      )
        .then(() => {
          toast.success("Message sent successfully!", { timeout: 3000 });
          this.userName = "";
          this.userEmail = "";
          this.userPhone = "";
          this.userMessage = "";
        })
        .catch((error) => {
          toast.error("Failed sent message. Try again later!", {
            timeout: 3000,
          });
          console.error(error);
        });
    },
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