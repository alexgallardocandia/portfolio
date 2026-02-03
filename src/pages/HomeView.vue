<template>
  <main class="pt-20">

    <!-- HERO -->
    <section
      id="home"
      class="min-h-screen flex items-center bg-black text-white"
    >
      <div class="container mx-auto px-6">
        <div class="grid grid-cols-1 md:grid-cols-2 items-center gap-10">

          <!-- TEXTO -->
          <div>
            <h1 class="text-4xl md:text-5xl font-bold mb-4">
              Hola, Soy
              <span class="text-indigo-400"> {{ typedText }} </span>
              <span class="animate-pulse">|</span>
            </h1>

            <p class="text-gray-300 text-lg leading-relaxed max-w-xl">
              Profesional de sistemas con {{yearExperience}} años de experiencia en infraestructura, desarrollo de software, y formación en Análisis de Sistemas.
            </p>
            <p class="text-gray-300 text-lg leading-relaxed max-w-xl">
              A lo largo de mi carrera he participado activamente en el relevamiento de requerimientos con usuarios, análisis de procesos, definición de funcionalidades y acompañamiento durante la implementación de soluciones.
            </p>
            <p class="text-gray-300 text-lg leading-relaxed max-w-xl">
              Participando en proyectos donde actúo como nexo entre el área técnica y el usuario final, asegurando que las soluciones desarrolladas respondan a las necesidades reales del negocio.
            </p>
          </div>

          <!-- IMAGEN -->
          <div class="flex justify-center md:justify-end">
            <img
              src="@/assets/alex_ida.png"
              alt="Alexander"
              class="w-80 md:w-[500px] lg:w-[600px]"
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
            <div class="bg-gray-50 p-6 rounded-xl shadow-md">
            <div class="w-14 h-14 bg-gray-200 rounded-full flex items-center justify-center mb-4">
                <!-- Icono -->
                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="size-6">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M12 21a9.004 9.004 0 0 0 8.716-6.747M12 21a9.004 9.004 0 0 1-8.716-6.747M12 21c2.485 0 4.5-4.03 4.5-9S14.485 3 12 3m0 18c-2.485 0-4.5-4.03-4.5-9S9.515 3 12 3m0 0a8.997 8.997 0 0 1 7.843 4.582M12 3a8.997 8.997 0 0 0-7.843 4.582m15.686 0A11.953 11.953 0 0 1 12 10.5c-2.998 0-5.74-1.1-7.843-2.918m15.686 0A8.959 8.959 0 0 1 21 12c0 .778-.099 1.533-.284 2.253m0 0A17.919 17.919 0 0 1 12 16.5c-3.162 0-6.133-.815-8.716-2.247m0 0A9.015 9.015 0 0 1 3 12c0-1.605.42-3.113 1.157-4.418" />
                </svg>
            </div>
            <h3 class="text-lg font-semibold mb-2">Desarrollo Web</h3>
            <p class="text-gray-500 text-sm">Desarrollo de aplicaciones web modernas y responsivas.</p>
            </div>

            <!-- CARD (bajada) -->
            <div class="bg-gray-50 p-6 rounded-xl shadow-md mt-8">
            <div class="w-14 h-14 bg-gray-200 rounded-full flex items-center justify-center mb-4">
                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="size-6">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M7.5 21 3 16.5m0 0L7.5 12M3 16.5h13.5m0-13.5L21 7.5m0 0L16.5 12M21 7.5H7.5" />
                </svg>
            </div>
            <h3 class="text-lg font-semibold mb-2">APIs REST</h3>
            <p class="text-gray-500 text-sm">Desarrollo de APIs REST para integrar sistemas.</p>
            </div>

            <!-- CARD -->
            <div class="bg-gray-50 p-6 rounded-xl shadow-md">
            <div class="w-14 h-14 bg-gray-200 rounded-full flex items-center justify-center mb-4">
                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="size-6">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M19.5 14.25v-2.625a3.375 3.375 0 0 0-3.375-3.375h-1.5A1.125 1.125 0 0 1 13.5 7.125v-1.5a3.375 3.375 0 0 0-3.375-3.375H8.25m2.25 0H5.625c-.621 0-1.125.504-1.125 1.125v17.25c0 .621.504 1.125 1.125 1.125h12.75c.621 0 1.125-.504 1.125-1.125V11.25a9 9 0 0 0-9-9Z" />
                </svg>
            </div>
            <h3 class="text-lg font-semibold mb-2">Documentación</h3>
            <p class="text-gray-500 text-sm">Documentación de sistemas y procesos.</p>
            </div>

            <!-- CARD (bajada) -->
            <div class="bg-gray-50 p-6 rounded-xl shadow-md mt-8">
            <div class="w-14 h-14 bg-gray-200 rounded-full flex items-center justify-center mb-4">
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
      class="min-h-screen bg-gray-100 text-gray-900 flex items-center"
    >
      <div class="container mx-auto px-6 max-w-4xl">
        <div class="grid grid-cols-1 md:grid-cols-2 gap-12">

          <!-- TEXTO -->
          <div>
            <h2 class="text-4xl font-bold mb-4">Contacto</h2>
            <p class="text-gray-600">
              ¿Tenés un proyecto en mente o querés trabajar conmigo?
              Completá el formulario y te respondo a la brevedad.
            </p>
          </div>

          <!-- FORMULARIO -->
          <form @submit.prevent="sendEmail" class="bg-white p-8 rounded-xl shadow-lg space-y-6">

            <div>
              <label class="block text-sm font-medium mb-1">Nombre</label>
              <input
                v-model="form.name"
                type="text"
                required
                class="w-full border border-gray-300 rounded-lg px-4 py-2 focus:outline-none focus:ring-2 focus:ring-indigo-500"
              />
            </div>

            <div>
              <label class="block text-sm font-medium mb-1">Email</label>
              <input
                v-model="form.email"
                type="email"
                required
                class="w-full border border-gray-300 rounded-lg px-4 py-2 focus:outline-none focus:ring-2 focus:ring-indigo-500"
              />
            </div>

            <div>
              <label class="block text-sm font-medium mb-1">Mensaje</label>
              <textarea
                v-model="form.message"
                rows="4"
                required
                class="w-full border border-gray-300 rounded-lg px-4 py-2 focus:outline-none focus:ring-2 focus:ring-indigo-500"
              ></textarea>
            </div>

            <button
              type="submit"
              class="w-full bg-indigo-600 text-white py-3 rounded-lg font-semibold hover:bg-indigo-700 transition"
            >
              Enviar mensaje
            </button>

            <p v-if="success" class="text-green-600 text-sm text-center">
              Mensaje enviado correctamente ✔
            </p>

            <p v-if="error" class="text-red-600 text-sm text-center">
              Ocurrió un error, intentá nuevamente ❌
            </p>

          </form>

        </div>
      </div>
    </section>

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
})
</script>
