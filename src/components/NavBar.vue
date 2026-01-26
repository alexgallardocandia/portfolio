<template>
  <nav class="fixed top-0 w-full z-50 bg-white/80 backdrop-blur shadow">
    <div class="max-w-6xl mx-auto px-4">
      <div class="flex justify-between items-center h-16">

        <!-- Logo -->
        <div class="flex items-center cursor-pointer" @click="scrollTo('home')">
          <img src="../assets/logo_AG-Photoroom.png" class="w-12" />
        </div>

        <!-- Desktop menu -->
        <div class="hidden md:flex space-x-8 font-medium">
          <button @click="scrollTo('home')" class="hover:text-indigo-600 transition">
            Inicio
          </button>
          <button @click="scrollTo('services')" class="hover:text-indigo-600 transition">
            Servicios
          </button>
          <button @click="scrollTo('contact')" class="hover:text-indigo-600 transition">
            Contacto
          </button>
        </div>

        <!-- Mobile button -->
        <button @click="toggleMobileMenu" class="md:hidden">
          <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path
              v-if="!mobileMenuOpen"
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M4 6h16M4 12h16M4 18h16"
            />
            <path
              v-else
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M6 18L18 6M6 6l12 12"
            />
          </svg>
        </button>
      </div>
    </div>

    <!-- Mobile menu -->
    <div
      v-if="mobileMenuOpen"
      class="md:hidden bg-white shadow-lg"
    >
      <button @click="mobileScroll('home')" class="block w-full px-6 py-4 text-left hover:bg-gray-100">
        Inicio
      </button>
      <button @click="mobileScroll('services')" class="block w-full px-6 py-4 text-left hover:bg-gray-100">
        Servicios
      </button>
      <button @click="mobileScroll('contact')" class="block w-full px-6 py-4 text-left hover:bg-gray-100">
        Contacto
      </button>
    </div>
  </nav>
</template>
<script setup>
import { ref } from 'vue'

const mobileMenuOpen = ref(false)

const toggleMobileMenu = () => {
  mobileMenuOpen.value = !mobileMenuOpen.value
}

const scrollTo = (id) => {
  const section = document.getElementById(id)
  if (section) {
    section.scrollIntoView({ behavior: 'smooth' })
  }
}

const mobileScroll = (id) => {
  scrollTo(id)
  mobileMenuOpen.value = false
}
</script>
