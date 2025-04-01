<template>
  <div>
    <Hero />
    <TrustedPartners />
    <VendorSupport />
    <WholesalersSection />
    <AccomplishmentsSection />
  </div>
</template>

<script setup>
definePageMeta({
  pageTransition: {
    name: "fade",
    mode: "out-in",
  },
});
import Hero from "~/components/Hero.vue";
import TrustedPartners from "~/components/TrustedPartners.vue";
import VendorSupport from "~/components/VendorSupport.vue";
import WholesalersSection from "~/components/WholesalersSection.vue";
import AccomplishmentsSection from "~/components/AccomplishmentsSection.vue";
</script>
