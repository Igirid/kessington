<template>
  <Transition :name="$route.meta.pageTransition?.name || 'fade'" mode="out-in">
    <div class="min-h-screen bg-white px-4 py-2">
      <Navbar />
      <NuxtPage />
      <Footer />
    </div>
  </Transition>
</template>

<script setup>
import Navbar from "~/components/Navbar.vue";
import Footer from "~/components/Footer.vue";
</script>

<style>
/* Default Fade Transition */
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s ease, transform 0.5s ease;
}

.fade-enter-from {
  opacity: 0;
  transform: translateY(200px);
  transform: scaleY(0px); /* Move up from bottom */
}

.fade-enter-to {
  opacity: 1;
  transform: translateY(0);
  transform: scaleY(400px); /* Move up from bottom */
}

.fade-leave-from {
  opacity: 1;
  transform: translateY(0);
}

.fade-leave-to {
  opacity: 0;
  transform: translateY(50px); /* Move down slightly when leaving */
}

/* Slide-Right Transition */
/* Slide from RIGHT to LEFT (Only on Enter) */
.slide-right-enter-active {
  transition: all 0.8s ease;
}

.slide-right-enter-from {
  opacity: 0;
  transform: translateX(600px); /* Enter from RIGHT */
}

.slide-right-enter-to {
  opacity: 1;
  transform: translateX(0);
}

/* No leave transition - Default behavior (fade out) */
</style>
