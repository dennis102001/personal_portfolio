<script setup>
import { ref } from 'vue';

const showSmallScreenMenu = ref(false)

</script>

<template>
  <div class="fixed top-6 w-full px-4 sm:px-8 md:px-12 ">
    <nav class="z-50
      max-w-5xl mx-auto
      rounded-full border border-slate-200/80 bg-white/80 backdrop-blur-xl shadow-lg
      "
    >
      <div class="flex items-center justify-between px-7 py-4">
        <a
          href="#hero"
          class="text-lg font-bold tracking-wide text-slate-900"
        >
          dennis<span class="text-blue-700">.</span>dev
        </a>

        <div class="hidden md:flex items-center gap-8">
          <a href="#about" class="text-slate-600 hover:text-blue-700 transition">About</a>
          <a href="#projects" class="text-slate-600 hover:text-blue-700 transition">Projects</a>
          <a href="#contact" class="text-slate-600 hover:text-blue-700 transition">Contact</a>
          <a href="#experience" class="text-slate-600 hover:text-blue-700 transition">Experience</a>
        </div>

        <a
          href="resume/Dennis_Bedana_Resume.pdf" target="_blank" rel="noopener noreferrer" title="Download my resume (PDF)"
          class="hidden md:inline-flex items-center rounded-full bg-slate-900 px-5 py-2 text-sm font-medium text-white transition hover:bg-slate-700"
        >
          Resume
        </a>

        <button @click="showSmallScreenMenu = true " class="md:hidden cursor-pointer hover:bg-slate-100 px-3 py-1 rounded-md transition-all grid place-items-center">
          <i class="fa-solid fa-bars"></i>
        </button>
      </div>
    </nav>
  </div>
  
  <div v-if="showSmallScreenMenu" class="md:hidden fixed z-50 text-white bg-slate-800/90 backdrop-blur-sm h-screen w-full flex flex-col items-center justify-center">
    
    <button @click="showSmallScreenMenu = false " class="absolute text-white text-xl z-50 top-4 right-4 cursor-pointer hover:bg-slate-600 active:bg-slate-600 px-3 py-2 rounded-md transition-all grid place-items-center">
      <i class="fa-solid fa-xmark"></i>
    </button>
      
    <nav class="flex flex-col items-center">
      <a
        href="#hero"
        @click="showSmallScreenMenu = false"
        class="text-lg font-bold mb-6 tracking-wide"
      >
        dennis<span class="text-blue-400">.</span>dev
      </a>

      <div class="flex flex-col items-center gap-2 w-sm">
        <a href="#about" @click="showSmallScreenMenu = false" class="hover:bg-slate-600 active:bg-slate-700 active:outline-1 hover:outline-1 transition px-4 py-2 w-full text-center rounded-md">About</a>
        <a href="#projects" @click="showSmallScreenMenu = false" class="hover:bg-slate-600 active:bg-slate-700 active:outline-1 hover:outline-1 transition px-4 py-2 w-full text-center rounded-md">Projects</a>
        <a href="#contact" @click="showSmallScreenMenu = false" class="hover:bg-slate-600 active:bg-slate-700 active:outline-1 hover:outline-1 transition px-4 py-2 w-full text-center rounded-md">Contact</a>
        <a href="#experience" @click="showSmallScreenMenu = false" class="hover:bg-slate-600 active:bg-slate-700 active:outline-1 hover:outline-1 transition px-4 py-2 w-full text-center rounded-md">Experience</a>
      </div>

      <a
        href="/resume/Dennis_Bedana_Resume.pdf"
        target="_blank"
        rel="noopener noreferrer" 
        title="Download my resume (PDF)"
        @click="showSmallScreenMenu = false"
        class="mt-6 rounded-full bg-white text-slate-900 px-6 py-2"
      >
        Resume
      </a>
    </nav>
  </div>

  <main>
    <RouterView/>
  </main>
</template>

<style scoped></style>
