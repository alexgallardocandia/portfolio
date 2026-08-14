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

    <!-- SOBRE MI / PERFIL -->
    <section
      id="about"
      class="py-24 bg-white text-gray-900"
    >
      <div class="container mx-auto px-6">
        <div class="max-w-3xl mx-auto text-center">
          <p class="text-indigo-600 uppercase tracking-widest mb-3">
            Sobre mí
          </p>
          <h2 class="text-4xl md:text-5xl font-bold mb-8 leading-tight">
            Lic. en Análisis de Sistemas Informáticos
          </h2>
          <p class="text-gray-500 text-lg leading-relaxed">
            Profesional en Análisis de Sistemas con experiencia en desarrollo de software,
            arquitectura de procesos e infraestructura. He participado activamente en el
            relevamiento de requerimientos con usuarios, análisis de flujos de negocio,
            definición de funcionalidades y acompañamiento en la implementación de
            soluciones. Actúo como nexo técnico-funcional entre el área de negocio y el
            equipo de desarrollo, asegurando soluciones eficientes y alineadas a los
            objetivos de la organización.
          </p>
        </div>
      </div>
    </section>

    <!-- EXPERIENCIA -->
    <section
      id="experience"
      class="py-24 bg-gray-50 text-gray-900"
    >
      <div class="container mx-auto px-6">
        <p class="text-indigo-600 uppercase tracking-widest mb-3 text-center">
          Trayectoria
        </p>
        <h2 class="text-4xl md:text-5xl font-bold mb-16 text-center leading-tight">
          Experiencia Laboral
        </h2>

        <div class="max-w-3xl mx-auto space-y-10 relative border-l-2 border-indigo-200 pl-8">

          <div v-for="job in experience" :key="job.company" class="relative">
            <span class="absolute -left-[39px] top-1.5 w-4 h-4 rounded-full bg-indigo-600 border-4 border-indigo-100"></span>
            <p class="text-sm font-semibold text-indigo-600">{{ job.period }}</p>
            <h3 class="text-xl font-bold mt-1">{{ job.role }}</h3>
            <p class="text-gray-500 font-medium mb-2">{{ job.company }}</p>
            <ul class="text-gray-500 text-sm leading-relaxed list-disc list-inside space-y-1">
              <li v-for="(task, i) in job.tasks" :key="i">{{ task }}</li>
            </ul>
          </div>

        </div>
      </div>
    </section>

    <!-- EDUCACION Y HABILIDADES -->
    <section
      id="skills"
      class="py-24 bg-white text-gray-900"
    >
      <div class="container mx-auto px-6">
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-16">

          <!-- EDUCACION -->
          <div>
            <p class="text-indigo-600 uppercase tracking-widest mb-3">Educación</p>
            <h2 class="text-2xl font-bold mb-6">Formación académica</h2>
            <div class="space-y-6">
              <div v-for="edu in education" :key="edu.institution">
                <p class="text-sm font-semibold text-indigo-600">{{ edu.period }}</p>
                <h3 class="font-bold">{{ edu.institution }}</h3>
                <p class="text-gray-500 text-sm">{{ edu.title }}</p>
              </div>
            </div>

            <p class="text-indigo-600 uppercase tracking-widest mb-3 mt-10">Idiomas</p>
            <ul class="text-gray-500 text-sm space-y-1">
              <li v-for="lang in languages" :key="lang">{{ lang }}</li>
            </ul>
          </div>

          <!-- HARD SKILLS -->
          <div>
            <p class="text-indigo-600 uppercase tracking-widest mb-3">Hard Skills</p>
            <h2 class="text-2xl font-bold mb-6">Habilidades técnicas</h2>
            <div class="flex flex-wrap gap-2">
              <span
                v-for="skill in hardSkills"
                :key="skill"
                class="bg-indigo-50 text-indigo-700 text-sm font-medium px-4 py-2 rounded-full"
              >
                {{ skill }}
              </span>
            </div>
          </div>

          <!-- SOFT SKILLS -->
          <div>
            <p class="text-indigo-600 uppercase tracking-widest mb-3">Soft Skills</p>
            <h2 class="text-2xl font-bold mb-6">Habilidades blandas</h2>
            <ul class="space-y-3">
              <li
                v-for="skill in softSkills"
                :key="skill"
                class="flex items-start gap-2 text-gray-500 text-sm"
              >
                <span class="w-1.5 h-1.5 mt-2 rounded-full bg-indigo-600 flex-shrink-0"></span>
                {{ skill }}
              </li>
            </ul>
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

    <!-- ICONOS FLOTANTES GLASS -->
    <div class="fixed bottom-24 right-8 flex flex-col gap-4 z-50">

      <!-- LINKEDIN -->
      <a
        href="https://www.linkedin.com/in/alexander-gallardo-a2b757265"
        target="_blank"
        class="group w-14 h-14 rounded-full
              bg-white/10 backdrop-blur-xl
              border border-white/20
              shadow-lg
              flex items-center justify-center
              transition-all duration-300
              hover:scale-110 hover:bg-indigo-500/20
              animate-float"
      >
        <svg xmlns="http://www.w3.org/2000/svg" x="0px" y="0px" width="40" height="40" viewBox="0 0 48 48">
          <path fill="#0288d1" d="M24 4A20 20 0 1 0 24 44A20 20 0 1 0 24 4Z"></path><path fill="#fff" d="M14 19H18V34H14zM15.988 17h-.022C14.772 17 14 16.11 14 14.999 14 13.864 14.796 13 16.011 13c1.217 0 1.966.864 1.989 1.999C18 16.11 17.228 17 15.988 17zM35 24.5c0-3.038-2.462-5.5-5.5-5.5-1.862 0-3.505.928-4.5 2.344V19h-4v15h4v-8c0-1.657 1.343-3 3-3s3 1.343 3 3v8h4C35 34 35 24.921 35 24.5z"></path>
        </svg>
      </a>

      <!-- WHATSAPP -->
      <a
        :href="whatsappLink"
        target="_blank"
        class="group w-14 h-14 rounded-full
              bg-white/10 backdrop-blur-xl
              border border-white/20
              shadow-xl
              flex items-center justify-center
              transition-all duration-300
              hover:scale-110 hover:bg-green-500/20
              animate-float"
      >
        <svg xmlns="http://www.w3.org/2000/svg" x="0px" y="0px" width="40" height="40" viewBox="0 0 48 48">
          <path fill="#fff" d="M4.868,43.303l2.694-9.835C5.9,30.59,5.026,27.324,5.027,23.979C5.032,13.514,13.548,5,24.014,5c5.079,0.002,9.845,1.979,13.43,5.566c3.584,3.588,5.558,8.356,5.556,13.428c-0.004,10.465-8.522,18.98-18.986,18.98c-0.001,0,0,0,0,0h-0.008c-3.177-0.001-6.3-0.798-9.073-2.311L4.868,43.303z"></path><path fill="#fff" d="M4.868,43.803c-0.132,0-0.26-0.052-0.355-0.148c-0.125-0.127-0.174-0.312-0.127-0.483l2.639-9.636c-1.636-2.906-2.499-6.206-2.497-9.556C4.532,13.238,13.273,4.5,24.014,4.5c5.21,0.002,10.105,2.031,13.784,5.713c3.679,3.683,5.704,8.577,5.702,13.781c-0.004,10.741-8.746,19.48-19.486,19.48c-3.189-0.001-6.344-0.788-9.144-2.277l-9.875,2.589C4.953,43.798,4.911,43.803,4.868,43.803z"></path><path fill="#cfd8dc" d="M24.014,5c5.079,0.002,9.845,1.979,13.43,5.566c3.584,3.588,5.558,8.356,5.556,13.428c-0.004,10.465-8.522,18.98-18.986,18.98h-0.008c-3.177-0.001-6.3-0.798-9.073-2.311L4.868,43.303l2.694-9.835C5.9,30.59,5.026,27.324,5.027,23.979C5.032,13.514,13.548,5,24.014,5 M24.014,42.974C24.014,42.974,24.014,42.974,24.014,42.974C24.014,42.974,24.014,42.974,24.014,42.974 M24.014,42.974C24.014,42.974,24.014,42.974,24.014,42.974C24.014,42.974,24.014,42.974,24.014,42.974 M24.014,4C24.014,4,24.014,4,24.014,4C12.998,4,4.032,12.962,4.027,23.979c-0.001,3.367,0.849,6.685,2.461,9.622l-2.585,9.439c-0.094,0.345,0.002,0.713,0.254,0.967c0.19,0.192,0.447,0.297,0.711,0.297c0.085,0,0.17-0.011,0.254-0.033l9.687-2.54c2.828,1.468,5.998,2.243,9.197,2.244c11.024,0,19.99-8.963,19.995-19.98c0.002-5.339-2.075-10.359-5.848-14.135C34.378,6.083,29.357,4.002,24.014,4L24.014,4z"></path><path fill="#40c351" d="M35.176,12.832c-2.98-2.982-6.941-4.625-11.157-4.626c-8.704,0-15.783,7.076-15.787,15.774c-0.001,2.981,0.833,5.883,2.413,8.396l0.376,0.597l-1.595,5.821l5.973-1.566l0.577,0.342c2.422,1.438,5.2,2.198,8.032,2.199h0.006c8.698,0,15.777-7.077,15.78-15.776C39.795,19.778,38.156,15.814,35.176,12.832z"></path><path fill="#fff" fill-rule="evenodd" d="M19.268,16.045c-0.355-0.79-0.729-0.806-1.068-0.82c-0.277-0.012-0.593-0.011-0.909-0.011c-0.316,0-0.83,0.119-1.265,0.594c-0.435,0.475-1.661,1.622-1.661,3.956c0,2.334,1.7,4.59,1.937,4.906c0.237,0.316,3.282,5.259,8.104,7.161c4.007,1.58,4.823,1.266,5.693,1.187c0.87-0.079,2.807-1.147,3.202-2.255c0.395-1.108,0.395-2.057,0.277-2.255c-0.119-0.198-0.435-0.316-0.909-0.554s-2.807-1.385-3.242-1.543c-0.435-0.158-0.751-0.237-1.068,0.238c-0.316,0.474-1.225,1.543-1.502,1.859c-0.277,0.317-0.554,0.357-1.028,0.119c-0.474-0.238-2.002-0.738-3.815-2.354c-1.41-1.257-2.362-2.81-2.639-3.285c-0.277-0.474-0.03-0.731,0.208-0.968c0.213-0.213,0.474-0.554,0.712-0.831c0.237-0.277,0.316-0.475,0.474-0.791c0.158-0.317,0.079-0.594-0.04-0.831C20.612,19.329,19.69,16.983,19.268,16.045z" clip-rule="evenodd"></path>
        </svg>
      </a>

    </div>


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

const phoneNumber = '595984586896' // tu número con código país sin +
const defaultMessage = 'Hola Alexander, te escribo porque vi tu portfolio y me gustaría conversar contigo.'

const whatsappLink = computed(() => {
  const encodedMessage = encodeURIComponent(defaultMessage)
  return `https://wa.me/${phoneNumber}?text=${encodedMessage}`
})


// EXPERIENCIA
const yearExperience = computed(() => {
  const startYear = 2019
  return new Date().getFullYear() - startYear
})

const experience = [
  {
    period: '2025 - Actual',
    role: 'Consultor de Sistemas de TI',
    company: 'IDESA',
    tasks: [
      'Análisis funcional y relevamiento de requerimientos para optimización de procesos internos.',
      'Diseño de arquitectura lógica e integración de servicios con pasarelas de pago y entidades externas.',
      'Consultoría técnica y soporte evolutivo sobre sistemas core y bases de datos.'
    ]
  },
  {
    period: '2024 - 2025',
    role: 'Desarrollador Web',
    company: 'BIX S.A.',
    tasks: [
      'Desarrollo de APIs para la app, correcciones e implementación de nuevos módulos en el sistema.',
      'Optimización de crons y procesos automáticos.'
    ]
  },
  {
    period: '2023 - 2024',
    role: 'Desarrollador Web',
    company: 'Grupo EPEM',
    tasks: [
      'Relevamiento y seguimiento de tickets, desarrollo de nuevas funcionalidades.',
      'Capacitación y trabajo en equipo.'
    ]
  },
  {
    period: '2019 - 2023',
    role: 'Auxiliar de Infraestructura',
    company: 'CHACOMER SAE',
    tasks: [
      'Servicio técnico al cliente interno, atención, mantenimiento, instalación, diagnóstico y gestión de recursos.'
    ]
  }
]

const education = [
  {
    period: '2020 - 2025',
    institution: 'Universidad Tecnológica Intercontinental',
    title: 'Licenciatura en Análisis y Diseño de Sistemas Informáticos'
  },
  {
    period: '2015 - 2018',
    institution: 'Colegio Nacional R. A. Fariña',
    title: 'Bachillerato Técnico en Informática'
  }
]

const languages = [
  'Español - Nativo',
  'Inglés - Técnico/Básico (Lectura y documentación)'
]

const hardSkills = [
  'Análisis Funcional y BPMN',
  'Relevamiento de Requerimientos',
  'Diseño e Integración de APIs REST',
  'SQL / Bases de Datos Relacionales',
  'PHP (Laravel / Slim / Symfony)',
  'Docker & Entornos Linux',
  'Git & Control de Versiones'
]

const softSkills = [
  'Capacidad Analítica y Resolución de Problemas',
  'Nexo Técnico-Funcional (Negocio/TI)',
  'Trabajo en Equipo y Adaptabilidad'
]

onMounted(() => {
  typeEffect()
  window.addEventListener('scroll', handleScroll)
})

</script>
<style scoped>
html {
  scroll-behavior: smooth;
}
@keyframes float {
  0% { transform: translateY(0px); }
  50% { transform: translateY(-6px); }
  100% { transform: translateY(0px); }
}

.animate-float {
  animation: float 3s ease-in-out infinite;
}

</style>
