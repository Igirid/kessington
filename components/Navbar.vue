<template>
  <nav
    class="top-10 z-50 bg-primary-blue px-4 md:px-8 py-4 rounded-t-3xl"
    :class="{
      'rounded-b-3xl':
        activeLink === '/contact' || activeLink === '/private-label',
    }"
  >
    <div class="mx-auto flex justify-between items-center">
      <!-- Logo -->
      <div class="w-16 h-16">
        <img
          src="/images/logo.png"
          alt="Logo"
          class="w-full h-full object-contain"
        />
      </div>

      <!-- Desktop Navigation -->
      <div
        class="hidden font-ibm md:flex items-center space-x-6 border-[1px] border-tiniest-border rounded-lg p-2"
      >
        <NuxtLink
          v-for="link in navLinks"
          :key="link.to"
          :to="link.to"
          class="nav-link relative flex items-center space-x-6 text-sm font-light border-[1px] border-tiniest-border rounded-lg transition-all duration-300 ease-in-out overflow-hidden text-gray-500"
          :class="{
            // 'py-0' : link.label === 'CONTACT US',
            ' border-tiny-border text-gray-300': $route.path === link.to,
            'text-gray-400':
              $route.path !== link.to && link.label !== 'CONTACT US',
            'text-[ #DFF4FDCC] bg-[radial-gradient(81.3%_81.58%_at_52.97%_61.96%,rgba(45,139,187,0)_0%,rgba(45,139,187,0.25)_100%)] px-0 !py-0':
              link.label === 'CONTACT US',
            'bg-[#2D8BBB]':
              hoveredLink === '/contact' && link.label === 'CONTACT US',
          }"
          @mouseenter="hoveredLink = link.to"
          @mouseleave="hoveredLink = null"
          @click="activeLink = link.to"
        >
          <!-- Chevron Right Icon (Only for Contact Us) -->

          <!-- Background with height transition -->
          <div
            class="absolute left-0 bottom-0 w-full bg-white rounded-lg transition-height opacity-80 duration-500 ease-in-out"
            :class="{
              hidden: link.label === 'CONTACT US',
              'h-full': hoveredLink === link.to,
              'h-0': hoveredLink !== link.to || hoveredLink === null,
            }"
          ></div>

          <!-- Text Content -->
          <span
            class="relative z-10 transition-colors duration-300 inline-block w-full px-5 py-3"
            :class="[
              // hoveredLink === link.to && link.label !== 'CONTACT US'
              // ? 'text-[#00263F]'
              // : 'text-primary-text',

              activeLink === link.to ||
              hoveredLink === link.to
              ? 'text-gray-300 hover:text-gray-800 text-xs font-normal'
              : 'text-gray-400 hover:text-gray-800 text-xs',
              // link.label === 'CONTACT US' ?' border rounded-tr-md rounded-br-md' : ''
              link.label === 'CONTACT US' ? ' hover:text-white':''
            ]"
          >
            {{ link.label }}
          </span>

          <div v-if="link.label === 'CONTACT US'" class="pr-1.5">
            <LucideChevronRight
              :class="{ 'bg-primary-blue': hoveredLink === link.to }"
              class="text-tiny-border hover:text-[#2D8BBB] bg-[#2D8BBB] w-6 stroke-[1px] font-light rounded-sm"
            />
          </div>
        </NuxtLink>
      </div>

      <!-- Mobile Menu Button -->
      <button @click="isMenuOpen = !isMenuOpen" class="md:hidden text-prim">
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
            stroke-width="2"
            d="M4 6h16M4 12h16m-16 6h16"
          />
        </svg>
      </button>
    </div>
  </nav>
</template>

<script setup>
import { ref } from "vue";
import { LucideChevronRight } from "lucide-vue-next";

// Import Chevron Right Icon

const isMenuOpen = ref(false);
const hoveredLink = ref(null);
const activeLink = ref("/");

const navLinks = ref([
  { label: "HOME", to: "/" },
  { label: "ABOUT US", to: "/about" },
  { label: "PRIVATE LABEL MEDICINE", to: "/private-label" },
  { label: "CONTACT US", to: "/contact" }, // Contact Us Link
]);
</script>

<style scoped>
/* Force ultra-thin border */
.nav-link {
  border-width: 0.5px !important;
}

/* Background Height Expansion */
.transition-height {
  transition: height 0.5s ease-in;
}
</style>
