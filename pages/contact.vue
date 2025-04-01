<template>
  <div class="bg-white min-h-screen">
    <div class="flex flex-col items-start gap-8 py-6">
      <div
        class="bg-primary-blue rounded-3xl p-6 md:p-10 shadow-xl space-y-10 w-full"
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
            <div class="relative w-[calc(50%-4px)] h-full">
              <NuxtImg
                src="/images/img-contact.svg"
                alt="Background Image"
                class="w-full h-full object-cover rounded-xl"
              >
              </NuxtImg>
              <div
                class="absolute w-full bg-transparent inset-0 flex flex-col gap-6 p-16"
              >
                <div class="flex flex-col gap-y-6">
                  <div class="flex gap-6 font-mono items-start content-start">
                    <NuxtImg
                      height="15"
                      width="15"
                      src="/images/contact/call.svg"
                    >
                    </NuxtImg>
                    <div class="-mt-1">
                      <p class="text-gray-400 text-sm font-mono">CALL US</p>
                      <p class="text-gray-50 font-mono text-sm select-all">
                        234-909-331-3563
                      </p>
                    </div>
                  </div>
                  <NuxtImg class="relative -left-24" src="/images/Line.svg">
                  </NuxtImg>
                  <div class="flex gap-6 font-mono items-start content-center">
                    <NuxtImg
                      height="15"
                      width="15"
                      src="/images/contact/MAIL.svg"
                    >
                    </NuxtImg>
                    <div class="-mt-1">
                      <p class="text-gray-400 text-sm font-mono">EMAIL US</p>
                      <p class="text-gray-50 font-mono text-sm select-all">
                        ADMIN@KESSINGTONGLOBAL.COM
                      </p>
                    </div>
                  </div>
                  <NuxtImg class="" src="/images/Line.svg"> </NuxtImg>
                  <div class="flex gap-6 font-mono items-start content-center">
                    <NuxtImg
                      height="20"
                      width="20"
                      src="/images/contact/alarm_smart_wake.svg"
                    >
                    </NuxtImg>
                    <div class="-mt-1">
                      <p class="text-gray-400 text-sm font-mono">HOURS</p>
                      <p class="text-gray-50 font-mono text-sm select-all">
                        MON - FRI: 9AM - 5PM
                      </p>
                    </div>
                  </div>
                  <NuxtImg class="relative -left-24" src="/images/Line.svg">
                  </NuxtImg>
                  <div class="flex gap-6 font-mono items-start content-center">
                    <img
                      class="w-[25px] h-[25px]"
                      src="/images/contact/location_on.svg"
                    />

                    <div class="-mt-1">
                      <p class="text-gray-400 text-sm font-mono">
                        OFFICE ADDRESS
                      </p>
                      <p
                        class="text-gray-50 font-mono text-sm select-all text-pretty max-w-[90%]"
                      >
                        12, ELERUWA STREET, WEMABOD ESTATE, ADENIYI JONES,
                        IKEJA, LAGOS, NIGERIA.
                      </p>
                    </div>
                  </div>
                  <NuxtImg class="" src="/images/Line.svg"> </NuxtImg>

                  <div
                    class="bg-gray-800 cursor-pointer px-18 py-4 opacity-50 w-max"
                  >
                    <p class="text-sm text-white font-mono">Get Direction</p>
                  </div>
                </div>
              </div>
            </div>
            <div class="relative w-[calc(50%-4px)] h-full">
              <NuxtImg
                src="/images/img-contact2.svg"
                alt="Background Image"
                class="w-full h-full object-cover rounded-xl"
              >
              </NuxtImg>
              <div
                class="absolute w-full bg-transparent inset-0 flex flex-col gap-6 p-16"
              >
                <div class="flex flex-col gap-y-4">
                  <p class="text-gray-700 font-mono">SEND US A QUICK MESSAGE</p>
                  <p class="text-gray-500 text-sm font-mono">
                    WE WILL GET BACK TO YOU AT THE EARLIEST
                  </p>

                  <div class="space-y-8 my-10">
                    <ContactCustomInput
                      v-model="fullName"
                      :placeholder="'FULL NAME'"
                      type="text"
                    />
                    <ContactCustomInput
                      v-model="email"
                      :placeholder="'EMAIL ADDRESS'"
                      type="text"
                    />
                    <ContactCustomInput
                      v-model="message"
                      :placeholder="'MESSAGE'"
                      type="textarea"
                    />
                  </div>
                  <button
                    class="flex self-center uppercase items-center bg-primary-blue font-mono text-gray-200 px-4 text-sm cursor-pointer py-2 rounded-full transition w-max"
                  >
                    SEND MESSAGE
                    <LucideArrowRight
                      class="w-5 h-5 ml-2 stroke-[1px] stroke-tiny-border"
                    />
                  </button>
                </div>
              </div>
            </div>

            <!-- Second Image (Top Layer) -->
          </div>
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
const fullName = ref("");
const email = ref("");
const message = ref("");
// Form handling logic would go here
</script>

<style scoped>
h1,
h3 {
  font-family: "Neue Montreal", sans-serif;
}
</style>
