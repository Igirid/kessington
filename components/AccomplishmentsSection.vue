<template>
  <section class="relative">
    <!-- Accomplishments Section -->

    <div class="bg-[#0A192F] mt-[-5px]">
      <img src="../assets/images/valueImg2.png" alt="" />
    </div>

    <!-- Testimonials Section -->
    <div class="bg-[#E6F4F9] py-16 md:py-24 px-4 sm:px-6 md:px-8">
      <div class="max-w-7xl mx-auto">
        <h2
          class="text-3xl sm:text-4xl md:text-6xl font-medium text-[#00263F] mb-10 md:mb-16 leading-tight"
        >
          Our Customers<br />
          Have This To Say:
        </h2>

        <div class="grid md:grid-cols-2 gap-8 md:gap-12 items-center">
          <div class="relative">
            <!-- Quote -->
            <div
              class="text-[#00AEE9] text-7xl font-serif absolute -top-10 left-0"
            >
              <img src="/images/quote.png" alt="" />
            </div>
            <p
              class="text-lg md:text-3xl text-[#00263F] font-normal mb-6 pl-6 mt-5"
            >
              I can't express how grateful I am that I can access products in
              comfort and purchase at discounted prices. Business has been made
              seamless for me
            </p>
            <p class="text-xl font-normal text-[#00263FCC] pl-6 w-3/4">
              Client like Phar. Uba who lives at Enugu is excited about her
              business growth.
            </p>
          </div>

          <div class="rounded-xl overflow-hidden">
            <img
              src="/images/testimonial-client.png"
              alt="Happy client testimonial"
              class="w-full h-auto object-cover sm:h-[300px] md:h-[350px] lg:h-[400px]"
            />
          </div>
        </div>

        <!-- Pagination Dots -->
        <div class="flex justify-center mt-10 md:mt-12">
          <div class="w-12 h-1 bg-[#00263F] rounded-full mx-1"></div>
          <div class="w-8 h-1 bg-gray-300 rounded-full mx-1"></div>
          <div class="w-8 h-1 bg-gray-300 rounded-full mx-1"></div>
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
