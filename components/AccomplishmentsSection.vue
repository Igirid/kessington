<template>
  <section class="relative">
    <!-- Accomplishments Section -->

    <div class="bg-[#0A192F] mt-[-5px]">
      <img src="../assets/images/valueImg2.png" alt="" />
    </div>

    <!-- Testimonials Section -->
    <div class="py-16 md:py-24 px-4 sm:px-6 md:px-8">
      <div class="max-w-7xl mx-auto rounded-2xl">
        <p
          class="text-[64px] font-medium leading-tight text-[#00263F] mb-10 md:mb-16"
        >
          Our Customers<br />
          Have This To Say:

      </p>

        <div class="flex justify-between items-center rounded-2xl">
          <div class="flex bg-[#E2F5FD] flex-col py-8 pl-12 gap-3 grow w-[720px] h-[480px] relative rounded-2xl shadow-lg">
            <!-- Quote -->
            <div
              class="text-[#00AEE9] text-7xl font-serif relative left-2"
            >
              <img src="/images/quote.png" alt="" />
            </div>
            <p
              class="text-lg text-[36px] leading-tight text-[#00263F] font-normal mb-6 px-3"
            >
              I can't express how grateful I am that I can access products in
              comfort and purchase at discounted prices. Business has been made
              seamless for me
            </p>
            <p class="text-xl font-normal text-[#00263FCC] pl-3 w-3/4">
              Client like Phar. Uba who lives at Enugu is excited about her
              business growth.
            </p>
          </div>

          <div class="rounded-xl w-[560px] h-[480px] flex">
            <img
              src="/images/testimonial-client.png"
              alt="Happy client testimonial"
              class="w-full object-cover rounded-2xl"
            />
          </div>
        </div>

        <!-- Pagination Dots -->
        <div class="flex justify-center mt-10 md:mt-12 w-full">
          <div class="w-[30%] h-[2px] bg-[#2F8CBB] rounded-full"></div>
          <div class="w-1/3 grow h-[2px] bg-gray-300 rounded-full"></div>
          <div class=" w-1/3 grow h-[2px] bg-gray-300 rounded-full"></div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
// No additional script needed
</script>

<style scoped>
h2 {
  font-family: "Neue Montreal", sans-serif;
}

/* Responsive styling for stat cards */
@media (max-width: 640px) {
  .grid-cols-1 > div {
    max-width: 280px;
    margin-left: auto;
    margin-right: auto;
  }
}

/* Light pattern for stat cards */
.bg-\[\#051019\]::before {
  content: "";
  position: absolute;
  inset: 0;
  background-image: url("data:image/svg+xml,%3Csvg width='20' height='20' viewBox='0 0 20 20' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='%2380D4F7' fill-opacity='0.05' fill-rule='evenodd'%3E%3Ccircle cx='3' cy='3' r='1'/%3E%3C/g%3E%3C/svg%3E");
  opacity: 0.3;
}

/* Optional dot pattern inside cards */
.dot-pattern {
  background-image: url("data:image/svg+xml,%3Csvg width='20' height='20' viewBox='0 0 20 20' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='%2380D4F7' fill-opacity='0.05' fill-rule='evenodd'%3E%3Ccircle cx='3' cy='3' r='1'/%3E%3C/g%3E%3C/svg%3E");
  background-size: 20px 20px;
}
</style>
