<template>
  <section
    class="bg-[#00172C] py-20 md:py-24 px-4 sm:px-6 lg:px-8 relative overflow-hidden"
  >
    <!-- Background pattern/stars -->
    <div class="absolute inset-0 opacity-30">
      <div class="absolute top-0 left-0 w-full h-full">
        <div
          class="absolute w-2 h-2 bg-white rounded-full opacity-70"
          style="top: 10%; left: 5%"
        ></div>
        <div
          class="absolute w-1 h-1 bg-white rounded-full opacity-60"
          style="top: 25%; left: 15%"
        ></div>
        <div
          class="absolute w-1.5 h-1.5 bg-white rounded-full opacity-80"
          style="top: 15%; left: 30%"
        ></div>
        <div
          class="absolute w-1 h-1 bg-white rounded-full opacity-50"
          style="top: 35%; left: 20%"
        ></div>
        <div
          class="absolute w-2 h-2 bg-white rounded-full opacity-70"
          style="top: 20%; right: 15%"
        ></div>
        <div
          class="absolute w-1 h-1 bg-white rounded-full opacity-60"
          style="top: 40%; right: 25%"
        ></div>
        <div
          class="absolute w-1.5 h-1.5 bg-white rounded-full opacity-80"
          style="top: 10%; right: 35%"
        ></div>
        <div
          class="absolute w-1 h-1 bg-white rounded-full opacity-50"
          style="top: 30%; right: 10%"
        ></div>
        <div
          class="absolute w-2 h-2 bg-white rounded-full opacity-70"
          style="bottom: 20%; left: 10%"
        ></div>
        <div
          class="absolute w-1 h-1 bg-white rounded-full opacity-60"
          style="bottom: 30%; left: 25%"
        ></div>
        <div
          class="absolute w-1.5 h-1.5 bg-white rounded-full opacity-80"
          style="bottom: 15%; right: 30%"
        ></div>
        <div
          class="absolute w-1 h-1 bg-white rounded-full opacity-50"
          style="bottom: 35%; right: 15%"
        ></div>
      </div>
    </div>

    <div class="max-w-5xl mx-auto text-center relative z-10">
      <h2
        class="text-3xl sm:text-4xl md:text-5xl lg:text-6xl text-white font-medium mb-8 md:mb-10"
      >
        Interested In Becoming<br class="hidden sm:block" />
        A Distributor<br class="hidden sm:block" />
        For Kessington Global?
      </h2>

      <div class="mt-10">
        <a
          href="/contact"
          class="inline-flex items-center bg-white text-[#00172C] px-6 py-3 rounded-full font-medium transition-all hover:bg-opacity-90 group"
        >
          CONTACT US
          <svg
            class="w-5 h-5 ml-2 transform group-hover:translate-x-1 transition-transform"
            viewBox="0 0 24 24"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M13 17L18 12L13 7"
              stroke="currentColor"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
            <path
              d="M6 12H18"
              stroke="currentColor"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
          </svg>
        </a>
      </div>
    </div>
  </section>
</template>

<script setup>
// No additional script needed for this static component
</script>

<style scoped>
h2 {
  font-family: "Neue Montreal", sans-serif;
}
</style>
