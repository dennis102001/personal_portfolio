<script setup></script>

<template>
  <nav class="fixed top-0 left-0 w-full bg-white shadow z-50">
    <div class="mx-auto flex max-w-6xl justify-center gap-8 p-4">
      <a href="#about" class="hover:text-blue-600">About</a>
      <a href="#projects" class="hover:text-blue-600">Projects</a>
      <a href="#contact" class="hover:text-blue-600">Contact</a>
      <a href="#experience" class="hover:text-blue-600">Experience</a>
    </div>
  </nav>

  <main>
    <RouterView/>
  </main>
</template>

<style scoped></style>
