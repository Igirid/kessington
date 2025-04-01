<template>
  <main class="bg-white">
    <div class="">
      <section
        class="bg-primary-blue relative flex items-center justify-center lg:pt-33 pt-20 pb-24 px-6 md:px-12 lg:px-16"
      >
        <div
          class="max-w-[95rem] w-full flex flex-col text-center lg:text-start lg:flex-row items-center justify-center md:gap-36 gap-10 text-white"
        >
          <!-- Left Section -->
          <div class="space-y-6 max-w-[630px] md:flex-1">
            <div
              class="inline-flex items-center px-4 py-2 bg-[#E5F6FD] text-[#00263F] rounded-full text-xs font-medium"
            >
              ABOUT US
            </div>
            <h1
              class="text-3xl md:text-4xl lg:text-4xl text-[#DFF4FD] leading-tight"
            >
              We are a trusted pharmaceutical manufacturer dedicated to
              strengthening the healthcare supply chain across Nigeria and
              beyond.
            </h1>
          </div>

          <!-- Right Section -->
          <div
            class="text-sm md:text-base max-w-[544px] md:flex-1 flex flex-col justify-center text-[#DFF4FDCC] leading-relaxed"
          >
            <p>
              As a key player in the pharmaceutical industry, we specialize in
              producing high-quality medications and collaborating with
              wholesalers, distributors, and healthcare institutions to ensure
              patients receive life-saving treatments when they need them most.
            </p>
            <p class="">
              With a commitment to excellence, integrity, and innovation, we
              have built a reputation as a reliable partner in the healthcare
              ecosystem, delivering value and reliability at every step of the
              supply chain.
            </p>
          </div>
        </div>
      </section>

      <div
        class="mt-6 bg-[#DFF4FDCC] rounded-[24px] flex flex-col lg:flex-row items-center justify-center px-4"
      >
        <div
          class="space-y-6 max-w-[630px] md:flex-1 lg:py-10 py-6 lg:pt-20 lg:pb-26 lg:pr-[2.9rem]"
        >
          <div
            class="inline-flex items-center px-4 py-2 bg-[#00263F1A] text-[#00263F] rounded-full text-xs font-medium"
          >
            OUR MISSION
          </div>
          <h1
            class="text-sm md:text-base text-[#00263F] leading-tight lg:leading-[2rem]"
          >
            To be a leading force in the pharmaceutical industry, recognized for
            our unwavering commitment to quality, innovation, and patient care.
            We aim to transform healthcare delivery by building a robust,
            sustainable supply chain that ensures every patient has access to
            the medications they need, when they need them.
          </h1>
        </div>
        <div
          class="space-y-6 max-w-[630px] md:flex-1 lg:border-l lg:border-l-[#00263F14] lg:py-10 py-6 lg:pt-20 lg:pb-26 lg:pl-14"
        >
          <div
            class="inline-flex items-center px-4 py-2 bg-[#00263F1A] text-[#00263F] rounded-full text-xs font-medium"
          >
            ABOUT US
          </div>
          <h1
            class="text-sm md:text-base text-[#00263F] leading-tight lg:leading-[2rem]"
          >
            To be a leading force in the pharmaceutical industry, recognized for
            our unwavering commitment to quality, innovation, and patient care.
            We aim to transform healthcare delivery by building a robust,
            sustainable supply chain that ensures every patient has access to
            the medications they need, when they need them.
          </h1>
        </div>
      </div>
    </div>

    <div class="mt-6 p-8 bg-[#0A192F]">
      <AboutValue />
    </div>

    <div class="bg-[#0A192F] mt-[-5px]">
      <img src="../assets/images/valueImg2.png" alt="" />
    </div>
  </main>
</template>
<script lang="ts" setup>
definePageMeta({
  pageTransition: {
    name: "slide-right",
    mode: "out-in",
  },
});
</script>

<style scoped>
section {
  background-image: url("../assets/images/heroBg.png");
  background-size: 120% 120%;
  background-position: center;
  background-repeat: no-repeat;
  /* border-radius: 24px !important; */
}
</style>
