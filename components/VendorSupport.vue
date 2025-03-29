<template>
  <section class="relative px-10 bg-white">
    <!-- Top Section -->

    <div class="max-w-7xl mx-auto">
      <div class="pt-16 pb-6 mb-4">
        <div class="">
          <h2
            class="text-3xl md:text-6xl font-medium text-[#00263F] mb-10 leading-tight"
          >
            Vendor Support &<br />
            Private-Label<br />
            Medicines
          </h2>

          <!-- Main Image - Pharmacist with Tablet -->
          <div class="relative h-screen w-full overflow-hidden">
            <video
              class="w-full h-full absolute top-0 left-0 object-cover z-0"
              autoplay
              loop
              muted
              playsinline
            >
              <source src="/video/video-placeholder.mp4" type="video/mp4" />
            </video>
            <!-- Fallback image -->
            <img
              src="/images/pharmacist-tablet.png"
              alt="Pharmacist checking inventory on tablet"
              class="w-full h-full object-cover"
            />
          </div>
        </div>
      </div>

      <!-- Bottom Section with Features -->
      <div
        class="text-white relative bg-url('/images/shape-container.png') bg-[#00263F]"
      >
        <!-- Curved Edge -->
        <!-- <div
          class="absolute -top-16 right-0 w-[110px] h-32 bg-[#00263F] rounded-tl-3xl rounded-tr-2xl"
        ></div> -->

        <div class="max-w-7xl mx-auto px-4 md:px-8 py-16">
          <div class="max-w-3xl mx-auto">
            <h3
              class="text-3xl md:text-4xl lg:text-5xl mb-16 md:mb-20 text-center font-medium leading-tight"
            >
              Keep Your Shelves<br />Well-Stocked
            </h3>

            <!-- Feature List -->
            <div class="space-y-16 relative">
              <!-- Vertical Line -->
              <div
                class="absolute left-[28px] top-6 h-[calc(100%-48px)] md:left-[25px] pointer-events-none"
              >
                <svg width="2" height="100%" class="overflow-visible">
                  <line
                    x1="1"
                    y1="0"
                    x2="1"
                    y2="100%"
                    stroke="rgba(255, 255, 255, 0.1)"
                    stroke-width="2"
                    stroke-dasharray="4 4"
                  />
                </svg>
              </div>

              <!-- Feature 1 -->
              <div
                class="flex flex-col md:flex-row space-y-4 md:space-y-0 md:space-x-8"
              >
                <div class="md:w-16 flex items-start">
                  <div
                    class="w-12 h-12 rounded-md border border-white/30 flex items-center justify-center bg-[#00263F] relative z-10"
                  >
                    <svg
                      xmlns="http://www.w3.org/2000/svg"
                      class="h-6 w-6"
                      fill="none"
                      viewBox="0 0 24 24"
                      stroke="currentColor"
                    >
                      <path
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        stroke-width="1.5"
                        d="M20 7l-8-4-8 4m16 0l-8 4m8-4v10l-8 4m0-10L4 7m8 4v10M4 7v10l8 4"
                      />
                    </svg>
                  </div>
                </div>
                <div class="flex-1">
                  <h4 class="text-xl mb-2 font-medium">Top Deals</h4>
                  <p class="text-sm text-gray-300 leading-relaxed">
                    Get unbeatable prices on a wide range of top-sourced from
                    us. Ordering through us guarantees exceptional value while
                    meeting your needs efficiently.
                  </p>
                </div>
              </div>

              <!-- Feature 2 -->
              <div
                class="flex flex-col md:flex-row space-y-4 md:space-y-0 md:space-x-8"
              >
                <div class="md:w-16 flex items-start">
                  <div
                    class="w-12 h-12 rounded-md border border-white/30 flex items-center justify-center bg-[#00263F] relative z-10"
                  >
                    <svg
                      xmlns="http://www.w3.org/2000/svg"
                      class="h-6 w-6"
                      fill="none"
                      viewBox="0 0 24 24"
                      stroke="currentColor"
                    >
                      <path
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        stroke-width="1.5"
                        d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"
                      />
                    </svg>
                  </div>
                </div>
                <div class="flex-1">
                  <h4 class="text-xl mb-2 font-medium">Bulk Distribution</h4>
                  <p class="text-sm text-gray-300 leading-relaxed">
                    We specialize in large scale manufacturing and reliable
                    distribution to support our network of providers ensuring
                    timely delivery and consistent supply for all your
                    requirements.
                  </p>
                </div>
              </div>

              <!-- Feature 3 -->
              <div
                class="flex flex-col md:flex-row space-y-4 md:space-y-0 md:space-x-8"
              >
                <div class="md:w-16 flex items-start">
                  <div
                    class="w-12 h-12 rounded-md border border-white/30 flex items-center justify-center bg-[#00263F] relative z-10"
                  >
                    <svg
                      xmlns="http://www.w3.org/2000/svg"
                      class="h-6 w-6"
                      fill="none"
                      viewBox="0 0 24 24"
                      stroke="currentColor"
                    >
                      <path
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        stroke-width="1.5"
                        d="M3 10h18M7 15h1m4 0h1m-7 4h12a3 3 0 003-3V8a3 3 0 00-3-3H6a3 3 0 00-3 3v8a3 3 0 003 3z"
                      />
                    </svg>
                  </div>
                </div>
                <div class="flex-1">
                  <h4 class="text-xl mb-2 font-medium">Flexible Payments</h4>
                  <p class="text-sm text-gray-300 leading-relaxed">
                    Ease your cash flow by paying only when the stock is
                    dispensed to your patients. This system minimizes cash
                    tie-downs, reduces the risk of expired stock.
                  </p>
                </div>
              </div>
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
h3,
h4 {
  font-family: "Neue Montreal", sans-serif;
}

@media (max-width: 768px) {
  h2,
  h3 {
    font-size: 2rem;
    line-height: 1.2;
  }

  .icon-box {
    min-width: 48px;
  }
}
</style>
