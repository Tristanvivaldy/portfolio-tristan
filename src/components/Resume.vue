<template>
  <div class="bg-[#222222] text-white px-25 py-25 crimson-text-regular">
    <div
      class="title text-2xl tracking-[0.8rem] text-[#F68CC2] crimson-text-bold"
    >
      RESUME
    </div>
    <div class="grid grid-cols-12 mt-15">
      <div class="section-education col-span-6">
        <div class="text-2xl">
          <div class="sub-title crimson-text-semibold">Education</div>
          <div
            class="content-1-education w-10/12 h-24 mt-5 mb-15 bg-white rounded-lg text-black px-5 py-4"
          >
            <div class="grid grid-cols-12 justify-center items-center">
              <div class="col-span-9 text-2xl crimson-text-bold">
                SMAN 2 Kota Bekasi
              </div>
              <div class="col-span-3 text-lg text-end">2017-2020</div>
            </div>
            <div class="text-lg text-pink-600 crimson-text-semibold">
              Math & Science Major
            </div>
          </div>
          <div class="tree center-line absolute left-0 -mt-8">
            <div class="bg-white border-1 w-16 h-0"></div>
            <div class="relative left-16 -mt-20 bg-white border-1 w-0 h-41">
              <div
                class="point absolute -left-2 -top-1 bg-white w-4 h-4 border-1 rounded-full"
              ></div>
              <div
                class="point absolute -left-2 -bottom-1 bg-white w-4 h-4 border-1 rounded-full"
              ></div>
              <div class="line absolute bg-white top-1 border-1 w-9"></div>
              <div class="line absolute bg-white bottom-1 border-1 w-9"></div>
            </div>
          </div>
          <div
            class="content-1-education w-1/2 mt-5 mb-10 h-24 bg-white rounded-lg"
          ></div>
        </div>
        <div>Organization</div>
      </div>
      <div class="section-education col-span-6">Experience</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ResumeSection",
};
</script>

<style>
</style>