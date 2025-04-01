<template>
  <section class="relative min-h-[calc(100vh-80px)] bg-white">
    <!-- Background Container with Rounded Corners - No border -->
    <div
      class="absolute inset-0 overflow-hidden"
      style="
        background-image: url('/images/bg.svg');
        background-size: cover;
        background-position: center;
      "
    >
      <!-- Square Corner -->
    </div>

    <!-- Main Content -->
    <div class="relative max-w-7xl mx-auto h-full pt-16 pb-16 px-4 md:px-8">
      <div class="grid md:grid-cols-2 gap-16 items-center justify-between">
        <!-- Left Content -->
        <div class="text-primary-text space-y-4 pt-20">
          <h1 class="text-5xl md:text-[64px] font-medium leading-tight">
            Caring For Your<br />
            Health Is Our No.<br />
            One Priority
          </h1>
          <p
            class="text-[#DFF4FDE5] text-base max-w-lg font-normal leading-relaxed"
          >
            We are a leading manufacturer and distributor of a wide range of
            registered active products, supported by a network of over 700
            distributors throughout Nigeria.
          </p>
        </div>

        <!-- <div class="relative">
          <swiper
            :modules="[SwiperAutoplay]"
            :effect="'coverflow'"
            :grabCursor="true"
            :centeredSlides="true"
            :loop="true"
            :slidesPerView="'auto'"
            :coverflowEffect="{
              rotate: 0,
              stretch: 0,
              depth: 200,
              modifier: 2.5,
              slideShadows: false,
            }"
            :autoplay="{
              delay: 5000,
              disableOnInteraction: false,
            }"
            class="w-full h-full swiper-container"
          >
            <swiper-slide class="!w-[250px] bg-white p-4 rounded-lg">
              <div
                class="relative rounded-xl overflow-hidden shadow-lg bg-green-400"
              >
                <img
                  src="/images/pharmacy1.png"
                  alt="Patient Care"
                  class="w-full h-[312px] object-cover opacity-90 mb-2"
                />
                <div class="absolute bottom-0 left-0 right-0 bg-[#00263F] p-3">
                  <p class="text-white text-sm font-light text-center">
                    Patient Care
                  </p>
                </div>
              </div>
            </swiper-slide>

            <swiper-slide class="!w-[250px] bg-white p-4 rounded-lg">
              <div
                class="relative rounded-xl overflow-hidden shadow-lg bg-white border-0"
              >
                <img
                  src="/images/pharmacy3.png"
                  alt="Quality Certified"
                  class="w-full h-[312px] object-cover"
                />
                <div class="absolute bottom-0 left-0 right-0 bg-[#00263F] p-3">
                  <p class="text-white text-sm text-center font-medium">
                    Quality Certified
                  </p>
                </div>
              </div>
            </swiper-slide>

            <swiper-slide class="!w-[250px] bg-white p-4 rounded-lg">
              <div class="relative rounded-xl overflow-hidden shadow-lg">
                <img
                  src="/images/pharmacy2.png"
                  alt="Distribution"
                  class="w-full h-[312px] object-cover opacity-90"
                />
                <div class="absolute bottom-0 left-0 right-0 bg-[#00263F] p-3">
                  <p class="text-white text-sm font-light text-center">
                    Distribution
                  </p>
                </div>
              </div>
            </swiper-slide>
          </swiper>
        </div> -->

        <div
          class="relative w-[470px] h-[400px] flex items-center justify-center overflow-hidden"
        >
          <div
            v-for="(image, index) in images"
            :key="index"
            class="absolute transition-all duration-[2000ms] ease-in-out"
            :class="getImageClasses(index)"
          >
            <img
              :src="image"
              alt="Carousel Image"
              class="w-full h-full object-contain rounded-lg transition-opacity duration-[1500ms]"
            />
          </div>
        </div>
      </div>
    </div>

    <!-- Scroll Indicator -->

    <div
      class="bg-white w-35 h-20 absolute bottom-0 left-0 rounded-tr-3xl curves"
    >
      <div
        class="absolute bottom-3 left-10 w-12 h-12 rounded-full border border-primary-blue flex items-center justify-center bg-white cursor-pointer hover:bg-gray-50 transition-colors scroll-indicator"
        @click="scrollToBottom"
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="h-4 w-4 text-primary-blue"
          viewBox="0 0 20 20"
          fill="currentColor"
        >
          <path
            fill-rule="evenodd"
            d="M16.707 10.293a1 1 0 010 1.414l-6 6a1 1 0 01-1.414 0l-6-6a1 1 0 111.414-1.414L9 14.586V3a1 1 0 012 0v11.586l4.293-4.293a1 1 0 011.414 0z"
            clip-rule="evenodd"
          />
        </svg>
      </div>
    </div>
  </section>
</template>

<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
import { Autoplay } from "swiper/modules";
import "swiper/css";
import "swiper/css/effect-coverflow";
import "swiper/css/pagination";
import { ref, onMounted } from "vue";

// Swiper modules
const SwiperAutoplay = Autoplay;

const images = ref([
  "/images/hero/1.svg",
  "/images/hero/2.svg",
  "/images/hero/3.svg",
]);

const currentIndex = ref(0);

onMounted(() => {
  setInterval(() => {
    currentIndex.value = (currentIndex.value + 1) % images.value.length;
  }, 6000); // 2s delay + 0.8s animation duration
});

// const getImageClasses = (index) => {
//   if (index === currentIndex.value) {
//     return "z-20 scale-110 opacity-100"; // Front image (larger & full opacity)
//   }
//   if ((index + 1) % images.value.length === currentIndex.value) {
//     return "z-10 -translate-x-30 opacity-40 scale-80"; // Left image (faded, smaller)
//   }
//   return "z-10 translate-x-30 opacity-40 scale-80"; // Right image (faded, smaller)
// };

// const getImageClasses = (index) => {
//   const prevIndex = (currentIndex.value - 1 + images.value.length) % images.value.length;

//   if (index === currentIndex.value) {
//     return "z-10 scale-110 opacity-100 transition-[opacity,transform] duration-[2500ms]"; // Front (larger, full opacity)
//   }
//   if (index === prevIndex) {
//     return "z-0 -translate-x-24 opacity-50 scale-80 transition-none"; // Left (moves first, then fades)
//   }
//   return "z-0 translate-x-24 opacity-50 scale-80 transition-none"; // Right (moves first, then fades)
// };

const getImageClasses = (index) => {
  const total = images.value.length;
  const prevIndex = (currentIndex.value - 1 + total) % total;
  const nextIndex = (currentIndex.value + 1) % total;

  if (index === currentIndex.value) {
    return "z-10 scale-110 opacity-100 translate-x-0"; // **Front (Biggest, Full Opacity)**
  }
  if (index === prevIndex) {
    return "z-0 scale-80 opacity-50 -translate-x-[120px]"; // **Left (Moves left)**
  }
  if (index === nextIndex) {
    return "z-0 scale-80 opacity-50 translate-x-[120px]"; // **Right (Moves right)**
  }
  return "hidden"; // Hide extra images
};
</script>

<style scoped>
/* Ensure smooth transitions */
.transition-all {
  transition: transform 2s ease-in-out, opacity 1.5s ease-in-out;
}

.swiper-container {
  padding: 50px 0;
}

.swiper-slide {
  transition: transform 0.6s cubic-bezier(0.4, 0, 0.2, 1);
}

.swiper-slide-active {
  transform: scale(1.05);
  z-index: 10;
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
}

.swiper-slide-prev,
.swiper-slide-next {
  transform: scale(0.85);
  opacity: 0.7;
}

:deep(.swiper-pagination) {
  bottom: 0 !important;
}

:deep(.swiper-pagination-bullet) {
  background: rgba(255, 255, 255, 0.2);
}

:deep(.swiper-pagination-bullet-active) {
  background: white;
}

.scroll-indicator::after {
  content: "";
  position: absolute;
  width: 100%;
  height: 100%;
  border: 2px solid #2d8bbb;
  border-radius: 50%;
  animation: pulse 2s infinite;
}

.curves::after {
  content: "";
  position: absolute;
  width: 20px;
  height: 20px;

  border-bottom-left-radius: 40%;

  background-color: #00263f;
  z-index: 10;
  right: -19px;
  bottom: -1px;
}

@keyframes pulse {
  0% {
    transform: scale(1);
    opacity: 1;
  }
  100% {
    transform: scale(1.5);
    opacity: 0;
  }
}
</style>
