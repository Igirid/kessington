<template>
  <div class="py-5 bg-white space-y-10">
    <div class="bg-primary-blue min-h-screen rounded-3xl">
      <div class="flex flex-col items-start gap-8 p-10">
        <button
          class="py-2 px-4 font-mono bg-primary-text text-dark-bg rounded-3xl text-sm uppercase"
        >
          Private Label Medicine
        </button>
        <div class="grid grid-cols-2 md:grid-cols-3 w-full gap-6">
          <div
            v-for="product in products"
            :key="product.name"
            class="bg-slightly-dark py-4 h-[360px] rounded-2xl shadow-md border border-tiniest-border"
          >
            <div class="flex flex-col items-center justify-center gap-8">
              <img
                :src="product.image"
                :alt="product.name"
                class="object-cover w-[200px] h-[200px]"
              />
              <div class="flex flex-col justify-center items-center gap-4">
                <p class="text-xl uppercase text-gray-50">{{ product.name }}</p>
                <p class="font-light text-gray-200">
                  {{ product.description }}
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div
      class="relative mb-4 w-full h-[345px] bg-transparent rounded-lg overflow-hidden"
    >
      <!-- First Image (Bottom Layer) -->
      <img
        src="/public/images/shap-bg.png"
        alt="Background Image"
        class="absolute inset-0 w-full h-full object-right"
      />

      <!-- Second Image (Top Layer) -->
      <img
        src="/public/images/dots.svg"
        alt="Top Overlay"
        class="absolute inset-y-0 left-[25%] w-full h-full object-cover"
      />
      <div
        class="absolute top-12 left-[25%] flex flex-col items-start space-y-6"
      >
        <!-- Large Text -->
        <div class="w-[774px] flex flex-col justify-center items-center gap-10">
          <h1
            class="text-[64px] text-center text-balance font-bold text-primary-blue leading-tight"
          >
            To Order Any of Our Private-Label Medicines
          </h1>

          <!-- Button with Text & Icon -->
          <button
            class="flex uppercase items-center bg-primary-blue font-mono text-gray-200 px-4 text-sm cursor-pointer py-2 rounded-full transition"
          >
            Contact Us
            <LucideArrowRight
              class="w-5 h-5 ml-2 stroke-[1px] stroke-tiny-border"
            />
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
definePageMeta({
  pageTransition: {
    name: "fade",
    mode: "out-in",
  },
});
// Form handling logic would go here
const products = useProducts();
</script>

<style scoped>
h1,
h3 {
  font-family: "Neue Montreal", sans-serif;
}
</style>
