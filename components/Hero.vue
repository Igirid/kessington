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
      <div class="flex gap-4 items-center justify-between px-4 lg:px-12">
        <!-- Left Content -->

        <div class="text-primary-text space-y-[24px]">
          <p class="text-[40px] lg:text-[64px] font-medium leading-tight">
            Caring For Your<br />
            Health Is Our No.<br />
            One Priority
          </p>
          <p
            class="text-[#DFF4FDE5] text-base max-w-xs lg:max-w-lg font-normal leading-relaxed"
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

        <!-- <div
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
              class="w-full h-full object-cover rounded-lg"
            />
          </div>
        </div> -->
        <div
          class="relative w-[400px] lg:w-[450px] h-[400px] flex justify-start pl-24 pt-16 overflow-visible"
        >
          <TransitionGroup name="carousel" tag="div">
            <div
              v-for="(image, index) in images"
              :key="image"
              class="absolute transition-all duration-[2000ms] ease-in-out"
              :class="getImageClasses(index)"
            >
              <img
                :src="image"
                alt="Carousel Image"
                
                class="w-auto h-full max-w-full max-h-full object-contain rounded-lg"
              />
            </div>
          </TransitionGroup>
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
  "/images/hero/1.png",
  "/images/hero/2.png",
  "/images/hero/3.png",
]);

// const currentIndex = ref(0);
let intervalId = null;
const carouselIndex = ref(0);

// Function to update carousel index instead of modifying the array
const nextSlide = () => {
  carouselIndex.value = (carouselIndex.value + 1) % images.value.length;
};

onMounted(() => {
  intervalId = setInterval(nextSlide, 6000);
});

onUnmounted(() => {
  clearInterval(intervalId);
});

// Function to get dynamic classes based on index
// const getImageClasses = (index) => {
//   return {
//     "absolute w-[350px] z-10 opacity-100 scale-[120%] animate-to-left": index === 1,
//     "absolute z-0 opacity-50 scale-[90%] animate-to-right": index === 0,
//     "absolute z-0 opacity-50 scale-[90%] animate-to-middle ": index === 2,
//   };
// };
const getImageClasses = (index) => {
  const positions = [
    "animate-to-left z-10 opacity-100 scale-[100%]", // Center (active)
    "animate-to-right z-0 opacity-40 scale-[80%]", // Moving out
    "animate-to-middle z-0 opacity-40 scale-[80%]", // Moving in
  ];

  // Calculate new position based on current carousel index
  const positionIndex =
    (index - carouselIndex.value + images.value.length) % images.value.length;
  return `absolute h-auto ${positions[positionIndex]}`;
};
</script>

<style scoped>
/* Center Image (Current) */
.animate-to-left {
  transform: translateX(0) scale(1.2);
  opacity: 1;
}

/* Right Image (Moving Out) */
.animate-to-right {
  transform: translateX(100%) scale(0.9);
  opacity: 0.5;
}

/* Left Image (Moving In) */
.animate-to-middle {
  transform: translateX(-100%) scale(0.9);
  opacity: 0.5;
}

/* Vue TransitionGroup Animations */
.carousel-move {
  transition: transform 2s ease-in-out, opacity 1500s ease-in-out;
}
/* Ensure smooth transitions */


/* .carousel-enter-from .animate-to-middle,
.carousel-leave-to .animate-to-middle{

} */



/* .animate-to-right {
  animation: right 1s infinite ease-in-out z-0;
}
.animate-to-left {
  animation: middle 1s infinite ease-in-out z-0;
}
.animate-to-middle {
  animation: right 1s infinite ease-in-out z-10;
} */
</style>
