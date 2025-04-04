<template>
  <section class="relative py-16 px-4 md:px-8 bg-white">
    <div class="max-w-7xl mx-auto">
      <!-- About Section -->
      <div class="mb-14">
        <div
          class="inline-block px-4 py-2 bg-[#DFF4FD] rounded-full mb-6 md:mb-10"
        >
          <p class="font-ibm text-xs font-medium text-primary-blue uppercase"
            >ABOUT KESSINGTON HEALTH</p
          >
        </div>

        <div class="max-w-6xl">
          <h2
            class="text-2xl md:text-[40px] mb-6 md:mb-8 text-[#00263F] leading-normal"
          >
            Kessington Health, a trusted pharmaceutical manufacturer (Regd:
            Kessington Global Synergy Ltd), specializes in high-quality
            medications and strengthens healthcare supply chains across Nigeria.
            We collaborate with partners to ensure timely access to life-saving
            treatments for patients.
          </h2>
        </div>
      </div>

      <!-- Trusted Partners Section -->
      <div class="mb-16 md:mb-20">
        <div
          class="inline-block px-4 py-2 bg-[#DFF4FD] rounded-full mb-6 md:mb-10"
        >
          <span class="text-xs font-ibm font-medium text-primary-blue uppercase"
            >TRUSTED BY TOP PHARMACIES</span
          >
        </div>

        <!-- Desktop Partners Grid (visible on medium screens and up) -->
        <div class="hidden md:block">
          <swiper
            :modules="[SwiperAutoplay]"
            :slides-per-view="4"
            :space-between="32"
            :loop="true"
            :speed="8000"
            :allowTouchMove="false"
            :autoplay="{
              delay: 0,
              disableOnInteraction: false,
            }"
            class="w-full partner-swiper"
          >
            <swiper-slide>
              <div class="flex items-center justify-center h-16">
                <img
                  src="/images/partners/medplus.png"
                  alt="Medplus"
                  class="h-full object-contain"
                />
              </div>
            </swiper-slide>
            <swiper-slide>
              <div class="flex items-center justify-center h-16">
                <img
                  src="/images/partners/medplus.png"
                  alt="Medplus"
                  class="h-full object-contain"
                />
              </div>
            </swiper-slide>
            <swiper-slide>
              <div class="flex items-center justify-center h-16">
                <img
                  src="/images/partners/nettpharmacy.png"
                  alt="Nett Pharmacy"
                  class="h-full object-contain"
                />
              </div>
            </swiper-slide>
            <swiper-slide>
              <div class="flex items-center justify-center h-16">
                <img
                  src="/images/partners/healthplus.png"
                  alt="Health Plus"
                  class="h-full object-contain"
                />
              </div>
            </swiper-slide>
            <swiper-slide>
              <div class="flex items-center justify-center h-16">
                <img
                  src="/images/partners/healthplus.png"
                  alt="Health Plus"
                  class="h-full object-contain"
                />
              </div>
            </swiper-slide>
            <swiper-slide>
              <div class="flex items-center justify-center h-16">
                <img
                  src="/images/partners/assetpharmacy.png"
                  alt="Asset Pharmacy"
                  class="h-full object-contain"
                />
              </div>
            </swiper-slide>
            <swiper-slide>
              <div class="flex items-center justify-center h-16">
                <img
                  src="/images/partners/assetpharmacy.png"
                  alt="Asset Pharmacy"
                  class="h-full object-contain"
                />
              </div>
            </swiper-slide>
          </swiper>
        </div>

        <!-- Mobile Partners Slider (visible on small screens) -->
        <div class="md:hidden">
          <swiper
            :modules="[SwiperAutoplay]"
            :slides-per-view="2"
            :space-between="16"
            :loop="true"
            :speed="8000"
            :allowTouchMove="false"
            :autoplay="{
              delay: 0,
              disableOnInteraction: false,
            }"
            class="w-full partner-swiper"
          >
            <swiper-slide>
              <div class="flex items-center justify-center h-16">
                <img
                  src="/images/partners/medplus.png"
                  alt="Medplus"
                  class="h-full object-contain"
                />
              </div>
            </swiper-slide>
            <swiper-slide>
              <div class="flex items-center justify-center h-16">
                <img
                  src="/images/partners/nettpharmacy.png"
                  alt="Nett Pharmacy"
                  class="h-full object-contain"
                />
              </div>
            </swiper-slide>
            <swiper-slide>
              <div class="flex items-center justify-center h-16">
                <img
                  src="/images/partners/healthplus.png"
                  alt="Health Plus"
                  class="h-full object-contain"
                />
              </div>
            </swiper-slide>
            <swiper-slide>
              <div class="flex items-center justify-center h-16">
                <img
                  src="/images/partners/assetpharmacy.png"
                  alt="Asset Pharmacy"
                  class="h-full object-contain"
                />
              </div>
            </swiper-slide>
          </swiper>
        </div>
      </div>

      <!-- Popular Products Section -->
      <div>
        <div
          class="inline-block px-4 py-2 bg-[#DFF4FD] rounded-full mb-6 md:mb-10"
        >
          <span class="font-ibm text-xs font-medium text-[#00263F] uppercase"
            >POPULAR PRODUCTS</span
          >
        </div>

        <div class="mb-10">
          <!-- Mobile Products Slider (visible on small and medium screens) -->
          <div class="lg:hidden">
            <swiper
              :modules="[SwiperAutoplay, SwiperPagination]"
              :slides-per-view="1.2"
              :space-between="16"
              :pagination="{ clickable: true }"
              :breakpoints="{
                640: {
                  slidesPerView: 2.2,
                  spaceBetween: 20,
                },
              }"
              class="w-full product-swiper"
            >
              <!-- Product 1 -->
              <swiper-slide>
                <div class="bg-[#A2D2E2] p-6 rounded-lg overflow-hidden">
                  <div
                    class="h-48 sm:h-64 flex items-center justify-center mb-4"
                  >
                    <img
                      src="/images/products/loratidine.png"
                      alt="LORATIDINE"
                      class="max-h-full object-contain"
                    />
                  </div>
                </div>
              </swiper-slide>

              <!-- Product 2 -->
              <swiper-slide>
                <div class="bg-[#A2D2E2] p-6 rounded-lg overflow-hidden">
                  <div
                    class="h-48 sm:h-64 flex items-center justify-center mb-4"
                  >
                    <img
                      src="/images/products/kesartem.png"
                      alt="KESARTEM"
                      class="max-h-full object-contain"
                    />
                  </div>
                  <h3 class="text-xl font-medium text-[#1A1A1A] mb-1">
                    KESARTEM
                  </h3>
                  <p class="text-sm text-[#4D4D4D]">
                    Artemether 80mg & Lumefantrine 480mg Tablets
                  </p>
                </div>
              </swiper-slide>

              <!-- Product 3 -->
              <swiper-slide>
                <div class="bg-[#A2D2E2] p-6 rounded-lg overflow-hidden">
                  <div
                    class="h-48 sm:h-64 flex items-center justify-center mb-4"
                  >
                    <img
                      src="/images/products/ciprofloxacin.png"
                      alt="CIPROFLOXACIN"
                      class="max-h-full object-contain"
                    />
                  </div>
                  <h3 class="text-xl font-medium text-[#1A1A1A] mb-1">
                    CIPROFLOXACIN
                  </h3>
                  <p class="text-sm text-[#4D4D4D]">
                    Ciprofloxacin Tablets USP (500mg)
                  </p>
                </div>
              </swiper-slide>
            </swiper>
          </div>

          <!-- Desktop Products Grid (visible on large screens and up) -->
          <div class="hidden lg:block">
            <div class="relative">
              <!-- Products Grid -->
              <div class="grid grid-cols-3 gap-6">
                <!-- Product 1 -->

                <div>
                  <div class="bg-[#A2D2E2] p-6 rounded-lg overflow-hidden">
                    <div class="h-64 flex items-center justify-center mb-4">
                      <img
                        src="/images/products/loratidine.png"
                        alt="LORATIDINE"
                        class="max-h-full object-contain"
                      />
                    </div>
                  </div>

                  <div class="mt-4">
                    <h3 class="text-xl font-medium text-[#1A1A1A] mb-1">
                      LORATIDINE
                    </h3>
                    <p class="text-sm text-[#4D4D4D]">
                      Chewable Tablets USP 10mg
                    </p>
                  </div>
                </div>

                <!-- Product 2 -->

                <div>
                  <div class="bg-[#A2D2E2] p-6 rounded-lg overflow-hidden">
                    <div class="h-64 flex items-center justify-center mb-4">
                      <img
                        src="/images/products/kesartem.png"
                        alt="KESARTEM"
                        class="max-h-full object-contain"
                      />
                    </div>
                  </div>

                  <div class="mt-4">
                    <h3 class="text-xl font-medium text-[#1A1A1A] mb-1">
                      KESARTEM
                    </h3>
                    <p class="text-sm text-[#4D4D4D]">
                      Artemether 80mg & Lumefantrine 480mg Tablets
                    </p>
                  </div>
                </div>

                <!-- Product 3 -->

                <div>
                  <div class="bg-[#A2D2E2] p-6 rounded-lg overflow-hidden">
                    <div class="h-64 flex items-center justify-center mb-4">
                      <img
                        src="/images/products/ciprofloxacin.png"
                        alt="CIPROFLOXACIN"
                        class="max-h-full object-contain"
                      />
                    </div>
                  </div>

                  <div class="mt-4">
                    <h3 class="text-xl font-medium text-[#1A1A1A] mb-1">
                      CIPROFLOXACIN
                    </h3>
                    <p class="text-sm text-[#4D4D4D]">
                      Ciprofloxacin Tablets USP (500mg)
                    </p>
                  </div>
                </div>
              </div>

              <!-- Navigation Arrows -->
              <div class="flex justify-between items-center gap-4 mt-8">
                <button
                  class="w-12 h-12 border border-gray-300 rounded-sm flex items-center justify-center"
                >
                  <LucideArrowLeft class="w-5 h-5 text-primary-blue" />
                </button>

                <div class="flex justify-center mt-10 md:mt-12">
                  <div class="w-12 h-1 bg-[#00263F] rounded-full mx-1"></div>
                  <div class="w-8 h-1 bg-gray-300 rounded-full mx-1"></div>
                  <div class="w-8 h-1 bg-gray-300 rounded-full mx-1"></div>
                </div>

                <button
                  class="w-12 h-12 border border-gray-300 rounded-sm flex items-center justify-center"
                >
                  <LucideArrowRight class="w-5 h-5 text-primary-blue" />
                </button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
import { Autoplay, Pagination } from "swiper/modules";
import "swiper/css";
import "swiper/css/pagination";

import { LucideArrowLeft, LucideArrowRight } from "lucide-vue-next";

// Swiper modules
const SwiperAutoplay = Autoplay;
const SwiperPagination = Pagination;
</script>

<style scoped>
.partner-swiper {
  padding: 20px 0;
}

:deep(.swiper-slide),
:deep(.swiper-slide-active),
:deep(.swiper-slide-prev),
:deep(.swiper-slide-next) {
  opacity: 1 !important;
  transition: none !important;
  transform: none !important;
  z-index: 1 !important;
  box-shadow: none !important;
}

:deep(.swiper-wrapper) {
  transition-timing-function: linear !important;
  box-shadow: none !important;
}

:deep(.swiper-container) {
  box-shadow: none !important;
}

.product-swiper {
  padding: 20px 0 40px;
}

:deep(.swiper-pagination) {
  bottom: 0 !important;
}

:deep(.swiper-pagination-bullet) {
  background: rgba(0, 38, 63, 0.3);
}

:deep(.swiper-pagination-bullet-active) {
  background: var(--color-primary-blue);
}

/* Additional responsive adjustments */
@media (max-width: 768px) {
  h2 {
    font-size: 1.5rem;
    line-height: 1.3;
  }
}
</style>
