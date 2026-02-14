<template>
  <main class="pt-20">

    <!-- HERO -->
    <section
      id="home"
      class="min-h-screen flex items-center bg-gradient-to-br from-black via-gray-900 to-black text-white"
    >
      <div class="container mx-auto px-6">
        <div class="grid grid-cols-1 md:grid-cols-2 items-center gap-14">

          <!-- TEXTO -->
          <div>
            <p class="text-indigo-400 uppercase tracking-widest text-sm mb-3">
              Portfolio
            </p>

            <h1 class="text-4xl md:text-6xl font-extrabold mb-6 leading-tight">
              Hola, soy <br>
              <span class="text-indigo-400">{{ typedText }}</span>
              <span class="animate-pulse">|</span>
            </h1>

            <p class="text-gray-300 text-lg max-w-xl mb-6">
              Analista de Sistemas con {{ yearExperience }} años de experiencia en desarrollo,
              infraestructura y análisis funcional, creando soluciones alineadas al negocio.
            </p>

            <div class="flex gap-4">
              <a href="#contact"
                class="bg-indigo-600 hover:bg-indigo-700 px-6 py-3 rounded-lg font-semibold transition">
                Contactarme
              </a>
              <a href="#services"
                class="border border-gray-600 hover:border-indigo-400 px-6 py-3 rounded-lg transition">
                Ver servicios
              </a>
            </div>
          </div>

          <!-- IMAGEN -->
          <div class="relative flex justify-center md:justify-end">
            <div class="absolute -inset-4 bg-indigo-500/20 blur-3xl rounded-full"></div>
            <img
              src="@/assets/image.png"
              alt="Alexander Gallardo"
              class="relative w-80 md:w-[480px] drop-shadow-2xl"
            />
          </div>

        </div>
      </div>
    </section>

    <!-- SERVICIOS -->
    <section
    id="services"
    class="min-h-screen bg-white text-gray-900 flex items-center"
    >
    <div class="container mx-auto px-6">
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-16 items-center">

        <!-- TEXTO IZQUIERDA -->
        <div>
            <p class="text-gray-400 uppercase tracking-wide mb-2">
            Servicios
            </p>

            <h2 class="text-4xl md:text-5xl font-bold leading-tight mb-6">
            Tu meta, mi objetivo.
            </h2>
            <p class="text-gray-400 max-w-lg leading-relaxed">
            Busco resolver tus necesidades a través de soluciones innovadoras y eficientes. Con tecnología que se adapta a tus necesidades.
            </p>
        </div>

        <!-- CARDS DERECHA -->
        <div class="grid grid-cols-2 gap-8">

            <!-- CARD -->
            <div
              class="group bg-white p-6 rounded-2xl shadow-md hover:shadow-xl transition-all hover:-translate-y-1"
            >
              <div
                class="w-14 h-14 bg-indigo-100 text-indigo-600 rounded-xl flex items-center justify-center mb-4 group-hover:bg-indigo-600 group-hover:text-white transition"
              >
                <!-- Icono -->
                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="size-6">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M12 21a9.004 9.004 0 0 0 8.716-6.747M12 21a9.004 9.004 0 0 1-8.716-6.747M12 21c2.485 0 4.5-4.03 4.5-9S14.485 3 12 3m0 18c-2.485 0-4.5-4.03-4.5-9S9.515 3 12 3m0 0a8.997 8.997 0 0 1 7.843 4.582M12 3a8.997 8.997 0 0 0-7.843 4.582m15.686 0A11.953 11.953 0 0 1 12 10.5c-2.998 0-5.74-1.1-7.843-2.918m15.686 0A8.959 8.959 0 0 1 21 12c0 .778-.099 1.533-.284 2.253m0 0A17.919 17.919 0 0 1 12 16.5c-3.162 0-6.133-.815-8.716-2.247m0 0A9.015 9.015 0 0 1 3 12c0-1.605.42-3.113 1.157-4.418" />
                </svg>
              </div>

              <h3 class="text-lg font-semibold mb-2">
                Desarrollo Web
              </h3>

              <p class="text-gray-500 text-sm leading-relaxed">
                Aplicaciones web modernas, escalables y optimizadas para el negocio.
              </p>
            </div>

            <!-- CARD (bajada) -->
             <div
              class="group bg-white p-6 rounded-2xl shadow-md hover:shadow-xl transition-all hover:-translate-y-1"
            >
              <div
                class="w-14 h-14 bg-indigo-100 text-indigo-600 rounded-xl flex items-center justify-center mb-4 group-hover:bg-indigo-600 group-hover:text-white transition"
              >
                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="size-6">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M7.5 21 3 16.5m0 0L7.5 12M3 16.5h13.5m0-13.5L21 7.5m0 0L16.5 12M21 7.5H7.5" />
                </svg>
            </div>
            <h3 class="text-lg font-semibold mb-2">APIs REST</h3>
            <p class="text-gray-500 text-sm">Desarrollo de APIs REST para integrar sistemas.</p>
            </div>

            <!-- CARD -->
             <div
              class="group bg-white p-6 rounded-2xl shadow-md hover:shadow-xl transition-all hover:-translate-y-1"
            >
              <div
                class="w-14 h-14 bg-indigo-100 text-indigo-600 rounded-xl flex items-center justify-center mb-4 group-hover:bg-indigo-600 group-hover:text-white transition"
              >
                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="size-6">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M19.5 14.25v-2.625a3.375 3.375 0 0 0-3.375-3.375h-1.5A1.125 1.125 0 0 1 13.5 7.125v-1.5a3.375 3.375 0 0 0-3.375-3.375H8.25m2.25 0H5.625c-.621 0-1.125.504-1.125 1.125v17.25c0 .621.504 1.125 1.125 1.125h12.75c.621 0 1.125-.504 1.125-1.125V11.25a9 9 0 0 0-9-9Z" />
                </svg>
            </div>
            <h3 class="text-lg font-semibold mb-2">Documentación</h3>
            <p class="text-gray-500 text-sm">Documentación de sistemas y procesos.</p>
            </div>

            <!-- CARD (bajada) -->
             <div
              class="group bg-white p-6 rounded-2xl shadow-md hover:shadow-xl transition-all hover:-translate-y-1"
            >
              <div
                class="w-14 h-14 bg-indigo-100 text-indigo-600 rounded-xl flex items-center justify-center mb-4 group-hover:bg-indigo-600 group-hover:text-white transition"
              >
                <svg class="w-7 h-7 text-gray-700" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                    d="M3 10h18M3 14h18" />
                </svg>
            </div>
            <h3 class="text-lg font-semibold mb-2">Optimización</h3>
            <p class="text-gray-500 text-sm">Optimización de aplicaciones y sistemas.</p>
            </div>

        </div>
        </div>
    </div>
    </section>


    <!-- CONTACTO -->
    <section
      id="contact"
      class="min-h-screen bg-gradient-to-br from-gray-100 to-gray-200
            flex items-center py-20"
    >
      <div class="container mx-auto px-6">

        <div class="grid grid-cols-1 lg:grid-cols-2 gap-20 items-center">

          <!-- LADO IZQUIERDO -->
          <div>
            <p class="text-indigo-600 uppercase tracking-widest mb-3">
              Contacto
            </p>

            <h2 class="text-5xl font-bold mb-6 leading-tight">
              ¿Tenés un proyecto en mente?
            </h2>

            <p class="text-gray-600 text-lg max-w-lg leading-relaxed">
              Me encantaría escuchar tu idea y ayudarte a transformarla en una solución real.
              Completá el formulario y te respondo a la brevedad.
            </p>

            <!-- decoración opcional -->
            <div class="mt-10 w-32 h-1 bg-indigo-600 rounded-full"></div>
          </div>

          <!-- FORMULARIO -->
          <form
            @submit.prevent="sendEmail"
            class="bg-white p-10 rounded-2xl shadow-2xl space-y-6"
          >

            <div>
              <label class="block text-sm font-medium mb-1">Nombre</label>
              <input
                v-model="form.name"
                type="text"
                required
                class="w-full rounded-lg border border-gray-300 px-4 py-4
                focus:border-indigo-500 focus:ring-2 focus:ring-indigo-500/20
                transition"
              />
            </div>

            <div>
              <label class="block text-sm font-medium mb-1">Email</label>
              <input
                v-model="form.email"
                type="email"
                required
                class="w-full rounded-lg border border-gray-300 px-4 py-4
                focus:border-indigo-500 focus:ring-2 focus:ring-indigo-500/20
                transition"
              />
            </div>

            <div>
              <label class="block text-sm font-medium mb-1">Mensaje</label>
              <textarea
                v-model="form.message"
                rows="5"
                required
                class="w-full rounded-lg border border-gray-300 px-4 py-4
                focus:border-indigo-500 focus:ring-2 focus:ring-indigo-500/20
                transition"
              ></textarea>
            </div>

            <button
              type="submit"
              class="w-full bg-indigo-600 hover:bg-indigo-700
              active:scale-[0.98] text-white py-4 rounded-lg
              font-semibold text-lg transition-all"
            >
              Enviar mensaje
            </button>

            <p v-if="success" class="text-green-600 text-sm text-center animate-fade-in">
              Mensaje enviado correctamente
            </p>

            <p v-if="error" class="text-red-600 text-sm text-center">
              Ocurrió un error, intentá nuevamente
            </p>

          </form>

        </div>
      </div>
    </section>

    <!-- BOTON VOLVER ARRIBA -->
    <button
      v-show="showScrollTop"
      @click="scrollToTop"
      class="fixed bottom-8 right-8 bg-indigo-600 hover:bg-indigo-700
            text-white p-4 rounded-full shadow-lg
            transition-all duration-300 hover:scale-110"
    >
      <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="size-6">
        <path stroke-linecap="round" stroke-linejoin="round" d="M4.5 10.5 12 3m0 0 7.5 7.5M12 3v18" />
      </svg>
    </button>
</main>
</template>
<script setup>
import { ref, computed, onMounted } from 'vue'
import emailjs from '@emailjs/browser'

// FORMULARIO
const form = ref({
  name: '',
  email: '',
  message: ''
})

const success = ref(false)
const error = ref(false)

const showScrollTop = ref(false)

const handleScroll = () => {
  showScrollTop.value = window.scrollY > 300
}

const scrollToTop = () => {
  window.scrollTo({
    top: 0,
    behavior: 'smooth'
  })
}


// EMAIL
const sendEmail = async () => {
  success.value = false
  error.value = false

  try {
    await emailjs.send(
      'service_3lj4t1k',
      'template_eolupfg',
      {
        from_name: form.value.name,
        from_email: form.value.email,
        message: form.value.message,
      },
      'sdkv3fXyMqO80KByh'
    )

    success.value = true
    form.value = { name: '', email: '', message: '' }

  } catch (e) {
    error.value = true
  }
}

// TEXTO ANIMADO
const fullTexts = ['Alexander Gallardo', 'Analista de Sistemas']
const typedText = ref('')
const textIndex = ref(0)
const charIndex = ref(0)

const typeEffect = () => {
  if (charIndex.value < fullTexts[textIndex.value].length) {
    typedText.value += fullTexts[textIndex.value].charAt(charIndex.value)
    charIndex.value++
    setTimeout(typeEffect, 120)
  } else {
    setTimeout(eraseEffect, 1500)
  }
}

const eraseEffect = () => {
  if (charIndex.value > 0) {
    typedText.value = typedText.value.slice(0, -1)
    charIndex.value--
    setTimeout(eraseEffect, 80)
  } else {
    textIndex.value = (textIndex.value + 1) % fullTexts.length
    setTimeout(typeEffect, 500)
  }
}

// EXPERIENCIA
const yearExperience = computed(() => {
  const startYear = 2023
  return new Date().getFullYear() - startYear
})

onMounted(() => {
  typeEffect()
  window.addEventListener('scroll', handleScroll)
})

</script>
<style scoped>
html {
  scroll-behavior: smooth;
}
</style>
