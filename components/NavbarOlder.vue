<template>
  <nav class="top-10 z-50 bg-primary-blue px-4 md:px-8 py-4 rounded-t-3xl">
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
      <div class="hidden md:flex items-center space-x-4">
        <a
          href="/"
          class="px-5 py-3 bg-primary-blue text-primary-text text-sm font-light rounded-lg"
          >HOME</a
        >
        <a
          href="/about"
          class="px-5 py-3 text-[#677986] hover:text-prim text-sm font-light"
          >ABOUT US</a
        >
        <a
          href="/private-label"
          class="px-5 py-3 text-[#677986] hover:text-prim text-sm font-light"
          >PRIVATE LABEL MEDICINE</a
        >
        <a
          href="/contact"
          class="px-5 py-3 text-[#677986] hover:text-prim text-sm font-light"
          >CONTACT US</a
        >
        <button
          class="w-10 h-10 flex items-center justify-center bg-primary-blue rounded-lg"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-5 w-5 text-prim"
            viewBox="0 0 20 20"
            fill="currentColor"
          >
            <path
              fill-rule="evenodd"
              d="M7.293 14.707a1 1 0 010-1.414L10.586 10 7.293 6.707a1 1 0 011.414-1.414l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414 0z"
              clip-rule="evenodd"
            />
          </svg>
        </button>
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

      <!-- Mobile Navigation -->
      <div
        v-if="isMenuOpen"
        class="absolute top-full left-0 right-0 bg-[#0A1A24] md:hidden"
      >
        <div class="flex flex-col space-y-4 px-4 py-6">
          <a
            href="/"
            class="px-4 py-2 bg-primary-blue text-white text-sm font-light rounded-lg w-fit"
            >HOME</a
          >
          <a href="/about" class="px-4 py-2 text-[#677986] text-sm font-light"
            >ABOUT US</a
          >
          <a
            href="/private-label"
            class="px-4 py-2 text-[#677986] text-sm font-light"
            >PRIVATE LABEL MEDICINE</a
          >
          <a href="/contact" class="px-4 py-2 text-[#677986] text-sm font-light"
            >CONTACT US</a
          >
        </div>
      </div>
    </div>
  </nav>
</template>

<script setup>
import { ref } from "vue";

const isMenuOpen = ref(false);
</script>
