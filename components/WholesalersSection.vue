<template>
  <section class="relative py-12 sm:py-16 md:py-24 bg-white">
    <div class="max-w-7xl mx-auto">
      <div class="flex gap-6 sm:gap-8 md:gap-12">
        <!-- Left Column - Image -->
        <div class="rounded-xl overflow-hidden w-[477px] h-[773px]">
          <img
            src="/images/wholesaler-inventory.png"
            alt="Wholesaler checking inventory"
            class="grow-0 flex w-full object-cover"
          />
        </div>

        <!-- Right Column - Content -->
        <div
          class="bg-[#E6F4F9] rounded-xl p-6 w-[680px] flex flex-col grow px-[49px]"
        >
          <p
            class="text-[64px] font-bold text-[#00263F] mb-8 sm:mb-10 md:mb-12 leading-tight"
          >
            For Wholesalers &<br class="hidden sm:block" />
            Distributors
          </p>

          <!-- Timeline Features -->
          <div class="relative">
            <!-- Vertical Line -->
            <div
              class="absolute left-[16px] sm:left-[24px] top-2 bottom-20 w-[1px] h-[420px] bg-[#00263F]/20"
            ></div>

            <!-- Feature 1 -->
            <div class="relative mb-10 sm:mb-12 md:mb-16 pl-10 sm:pl-16">
              <div
                class="absolute left-0 top-0 flex items-center justify-center"
              >
                <div
                  class="w-12 h-12 px-2 bg-[#DFF4FD] border-[1px] border-gray-400 flex items-center justify-center"
                >
                  <img
                    src="/images/strategic.png"
                    class="w-5 h-5"
                    alt="Wholesaler Icon"
                  />
                </div>
              </div>
              <h3
                class="text-base sm:text-xl font-medium text-[#00263F] mb-2 sm:mb-3"
              >
                Strategic Collaboration:
              </h3>
              <p class="text-xs sm:text-sm text-[#445F6F] leading-relaxed">
                We prioritize partnerships with wholesalers and distributors to
                strengthen the supply chain, ensuring pharmacies, hospitals, and
                healthcare institutions receive life-saving medications
                efficiently and reliably.
              </p>
            </div>

            <!-- Feature 2 -->
            <div class="relative mb-10 sm:mb-12 md:mb-16 pl-10 sm:pl-16">
              <div
                class="absolute left-0 top-0 w-8 sm:w-12 h-8 sm:h-12 flex items-center justify-center"
              >
                <div
                  class="w-12 h-12 border-[1px] border-gray-400 bg-[#DFF4FD] flex items-center justify-center"
                >
                  <img
                    src="/images/verified.svg"
                    alt="Wholesaler Icon"
                    class="ml-2"
                  />
                  >
                </div>
              </div>
              <h3
                class="text-base sm:text-xl font-medium text-[#00263F] mb-2 sm:mb-3"
              >
                Unwavering Quality
              </h3>
              <p class="text-xs sm:text-sm text-[#445F6F] leading-relaxed">
                We prioritize partnerships with wholesalers and distributors to
                strengthen the supply chain, ensuring pharmacies, hospitals, and
                healthcare institutions receive life-saving medications
                efficiently and reliably.
              </p>
            </div>

            <!-- Feature 3 -->
            <div class="relative pl-10 sm:pl-16">
              <div
                class="absolute left-0 top-0 w-8 sm:w-12 h-8 sm:h-12 flex items-center justify-center"
              >
                <div
                  class="w-12 h-12 border-[1px] border-gray-400 bg-[#DFF4FD] shadow-sm flex items-center justify-center"
                >
                  <img src="/images/payments.png" alt="Wholesaler Icon" />
                </div>
              </div>
              <h3
                class="text-base sm:text-xl font-medium text-[#00263F] mb-2 sm:mb-3"
              >
                Streamlined Operations
              </h3>
              <p class="text-xs sm:text-sm text-[#445F6F] leading-relaxed">
                By fostering close partnerships, we streamline operations,
                maintain affordability, and ensure patients have consistent
                access to necessary medications. Together, we deliver value,
                trust, and reliability at every step of the healthcare supply
                chain.
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
// No additional script needed for this static component
</script>

<style scoped>
h2,
h3 {
  font-family: "Neue Montreal", sans-serif;
}

@media (max-width: 640px) {
  .relative.pl-10 {
    padding-left: 2.5rem;
  }

  .absolute.left-\[16px\] {
    left: 12px;
  }
}

@media (min-width: 641px) and (max-width: 768px) {
  .relative.pl-16 {
    padding-left: 3.5rem;
  }

  .absolute.left-\[24px\] {
    left: 20px;
  }
}

@media (min-width: 769px) and (max-width: 1024px) {
  h2 {
    font-size: 2.5rem;
  }
}
</style>
