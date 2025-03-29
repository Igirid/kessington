<template>
  <div class="min-h-screen bg-white px-4 py-2">
    <Navbar />
    <slot />
    <Footer />
  </div>
</template>

<script setup>
import Navbar from "~/components/Navbar.vue";
import Footer from "~/components/Footer.vue";
</script>
