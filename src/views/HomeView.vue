<script setup>
</script>

<template>
  <div class="min-h-screen bg-slate-50 p-6">
    <div
      class="max-w-6xl mx-auto bg-white rounded-[2rem] shadow-xl p-8 md:p-10"
    >
      <!-- Hero -->
      <div
        class="flex flex-col md:flex-row md:items-center md:justify-between gap-6 mb-10"
      >
        <div>
          <h1 class="text-4xl md:text-5xl font-bold bg-gradient-to-r from-slate-900 to-blue-900 bg-clip-text text-transparent">
            Dennis Bedaña
          </h1>

          <div class="inline-block mt-3 px-4 py-1 rounded-full bg-blue-50 border border-blue-100 text-blue-900 text-sm font-semibold">
            💻 Junior Full-Stack Developer
          </div>

          <p class="mt-4 max-w-lg text-slate-700">
            Building clean, functional web apps with a focus on user experience
            and modern JavaScript.
          </p>
        </div>

        <div class="flex items-center gap-3 px-6 py-3 rounded-full bg-blue-50 border border-blue-100">
          📍 Remote · Open to Work
        </div>
      </div>

      <!-- Contact -->
      <div
        class="flex flex-wrap gap-6 pb-8 mb-10 border-b border-slate-200 text-sm"
      >
        <a href="#" class="hover:text-blue-900">
          📧 dennisbed1001@gmail.com
        </a>

        <a href="#" class="hover:text-blue-900">
          🐙 github.com/dennis102001
        </a>

        <a href="#" class="hover:text-blue-900">
          💼 linkedin/in/dennis
        </a>

        <a href="#" class="hover:text-blue-900">
          📞 +639513754423
        </a>
      </div>

      <!-- About & Skills -->
      <div class="grid md:grid-cols-2 gap-10 mb-12">
        <div>
          <h2 class="uppercase font-semibold text-slate-600 mb-4">
            About
          </h2>

          <p class="text-slate-700 mb-4">
            Hi, I'm Dennis — a junior full-stack developer passionate about
            turning ideas into polished web experiences.
          </p>

          <p class="text-slate-700">
            Currently exploring more about web development and making personal projects.
          </p>
        </div>

        <div>
          <h2 class="uppercase font-semibold text-slate-600 mb-4">
            Tech Stack
          </h2>

          <div class="flex flex-wrap gap-2">
            <span
              v-for="skill in skills"
              :key="skill"
              class="px-4 py-2 rounded-full bg-blue-50 border border-blue-100 text-sm"
            >
              {{ skill }}
            </span>
          </div>
        </div>
      </div>

      <!-- Projects -->
      <div class="mb-12">
        <h2 class="uppercase font-semibold text-slate-600 mb-6">
          Featured Projects
        </h2>

        <div class="grid md:grid-cols-3 gap-6">
          <div
            v-for="project in projects"
            :key="project.title"
            class="p-6 rounded-3xl border border-slate-200 bg-slate-50 hover:bg-white hover:shadow-lg transition"
          >
            <h3 class="text-xl font-semibold text-slate-900">
              {{ project.title }}
            </h3>

            <p class="text-slate-600 mt-2">
              {{ project.description }}
            </p>

            <div class="flex flex-wrap gap-2 my-4">
              <span
                v-for="tag in project.tags"
                :key="tag"
                class="px-3 py-1 rounded-full bg-blue-100 text-xs font-semibold"
              >
                {{ tag }}
              </span>
            </div>

            <div class="flex gap-4 text-sm text-blue-900">
              <a href="#">Code</a>
              <a href="#">Demo</a>
            </div>
          </div>
        </div>
      </div>

      <!-- Experience & Education -->
      <div class="grid md:grid-cols-2 gap-10">
        <div>
          <h2 class="uppercase font-semibold text-slate-600 mb-4">
            Experience
          </h2>

          <div class="space-y-4">
            <div>
              <h3 class="font-semibold">
                Computer Programmer · (Part-time)
              </h3>
              <p class="text-sm text-slate-500">2024–2025</p>
              <ul class="list-disc list-inside text-slate-700 space-y-1 mt-1">
                <li>Collaborated with a team to develop a procurement and inventory management system</li>
                <li>Built desktop application using VB.NET, SQL Server, and Crystal Reports</li>
                <li>Currently transitioning to modern web development with Laravel + Vue.js and Tailwind CSS</li>
              </ul>
            </div>

            <div>
              <h3 class="font-semibold">
                Intern
              </h3>
              <p class="text-sm text-slate-500">2023–2024</p>
              <ul class="list-disc list-inside text-slate-700 space-y-1 mt-1">
                <li>Worked with a team to build a field findings and promissory note management system</li>
                <li>Developed using VB.NET, SQL Server, and Crystal Reports</li>
                <li>Gained experience in desktop development and team collaboration</li>
              </ul>
            </div>
          </div>
        </div>

        <div>
          <h2 class="uppercase font-semibold text-slate-600 mb-4">
            Education
          </h2>

          <div class="space-y-4">
            <div>
              <h3 class="font-semibold">
                B.S. Information Technology
              </h3>
              <p class="text-slate-500">
                Sultan Kudarat State University · 2024
              </p>
            </div>

          </div>
        </div>
      </div>

      <!-- Footer -->
      <div
        class="mt-12 pt-8 border-t border-slate-200 flex flex-col md:flex-row justify-between gap-4 text-slate-500"
      >
        <p>Crafted with ❤️ · 2026</p>

        <div class="flex gap-4">
          <a href="#">GitHub</a>
          <a href="#">LinkedIn</a>
          <a href="#">Resume</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const skills = [
  'PHP',
  'Laravel',
  'JavaScript',
  'Vue.js',
  'Tailwind CSS',
  'REST APIs',
  'MySql',
  'Git',
]

const projects = [
  {
    title: 'ChatTayo',
    description:
      'Real-time messaging web application.',
    tags: ['Vue.js', 'Laravel', 'MySql', 'Laravel Reverb', 'Laravel Echo', 'Tailwind CSS']
  },
  {
    title: 'Inventory Management System',
    description:
      'Inventory management system with status tracking for purchase and sales orders.',
    tags: ['Vue.js', 'Laravel', 'MySql', 'Chart.js', 'Tailwind CSS']
  },
  {
    title: 'ExpenseTracker',
    description:
      'Personal expense tracker developed using custom MVC architecture',
    tags: ['PHP', 'JavaScript', 'MySql', 'Tailwind CSS']
  }
]
</script>
