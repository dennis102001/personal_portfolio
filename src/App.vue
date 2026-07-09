<script setup></script>

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
          class="text-lg font-bold tracking-tight text-slate-900"
        >
          Dennis<span class="text-blue-700">.</span>
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

        <button class="md:hidden">
          <i class="fa-solid fa-bars"></i>
        </button>
      </div>
    </nav>
  </div>
  

  <main>
    <RouterView/>
  </main>
</template>

<style scoped></style>
