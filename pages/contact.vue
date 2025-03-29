<template>
  <div class="bg-white min-h-screen">
    <div class="flex flex-col items-start gap-8 py-8">
      <div
        class="bg-primary-blue rounded-xl p-6 md:p-10 shadow-xl space-y-10 w-full"
      >
        <button
          class="py-2 px-5 font-mono bg-primary-text text-dark-bg rounded-3xl text-sm uppercase"
        >
          Contact Us
        </button>
        <div class="space-y-10 flex flex-col">
          <!-- Contact Information -->
          <div class="w-[588px] h-[120px]">
            <!-- <h3 class="text-2xl text-white font-medium mb-6">Get in Touch</h3> -->
            <p class="text-gray-300 text-balance text-3xl">
              Got a question? Feedback?
              <span class="text-gray-400">
                Awesome! Send your message in the form below and we will get
                back to you as early as possible.
              </span>
            </p>
          </div>

          <!-- <div
            class="relative -mx-6 mb-4 w-full h-[400px] md:h-[580px] flex justify-between gap-x-12 bg-transparent rounded-lg overflow-hidden"
          >
            <img
              src="/public/images/img-contact.svg"
              alt="Background Image"
              class="w-[55%] h-[400px] md:h-full max-h-[580px] object-right -ml-2"
            />

            <img
              src="/public/images/img-contact2.svg"
              alt="Top Overlay"
              class="w-[45%] h-[400px] md:h-full max-h-[580px] object-cover rounded-lg"
            />
          </div> -->
          <div
            class="relative mb-4 w-full h-[400px] md:h-[580px] flex justify-between gap-x-8 bg-transparent rounded-lg overflow-hidden"
          >
            <!-- First Image (Bottom Layer) -->
            <img
              src="/images/img-contact.svg"
              alt="Background Image"
              class="w-[calc(50%-4px)] h-full object-cover rounded-xl"
            />

            <!-- Second Image (Top Layer) -->
            <img
              src="/images/img-contact2.svg"
              alt="Top Overlay"
              class="w-[calc(50%-4px)] h-full object-cover rounded-xl"
            />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
// Form handling logic would go here
</script>

<style scoped>
h1,
h3 {
  font-family: "Neue Montreal", sans-serif;
}
</style>
