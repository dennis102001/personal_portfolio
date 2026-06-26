<script setup>
</script>

<template>
  <div class="min-h-screen bg-slate-50 p-6">
    <div
      class="max-w-6xl mx-auto bg-white rounded-[2rem] shadow-xl p-8 md:p-10"
    >
      <!-- Hero -->
      <div class="flex flex-col md:flex-row md:items-center md:justify-between gap-6 mb-10">
        <div>
          <h1 class="text-4xl md:text-5xl font-bold bg-gradient-to-r from-slate-900 to-blue-900 bg-clip-text text-transparent">
            Dennis Bedaña
          </h1>

          <div class="inline-block mt-3 px-4 py-1 rounded-full bg-blue-50 border border-blue-100 text-blue-900 text-sm font-semibold">
            💻 Junior Full-Stack Web Developer
          </div>

          <p class="mt-4 max-w-lg text-slate-700">
            Junior Full-Stack Developer building modern, user-friendly web applications with Laravel and Vue.js.
          </p>
        </div>

        <div class="flex items-center gap-3 px-6 py-3 rounded-full bg-blue-50 border border-blue-100">
          <div v-if="openToWork">
            📍 Remote · Open to Work
          </div>

          <div v-else>
            📍 Philippines · Junior Full-Stack Developer
          </div>
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
          📞 +63 9513754423
        </a>
      </div>

      <!-- About & Experience -->
      <div class="grid md:grid-cols-2 gap-10 mb-12">
        <!-- About & Skills -->
        <div class="flex flex-col gap-10">

          <div>
            <h2 class="uppercase font-semibold text-slate-600 mb-4">
              About
            </h2>

            <p class="text-slate-700 mb-4">
              Hi, I'm Dennis, a Junior Full-Stack Web Developer passionate about building clean, functional, and user-friendly web applications. I enjoy turning ideas into real projects using Laravel, Vue.js, and Tailwind CSS, with a focus on creating simple and modern user experiences.
            </p>

            <p class="text-slate-700">
              I continuously improve my skills by building personal projects and learning new technologies, and I'm currently open to opportunities where I can grow as a developer and contribute to meaningful projects.
            </p>
          </div>

          <div>
            <h2 class="uppercase font-semibold text-slate-600 mb-4">
              Tech stack
            </h2>

            <div class="grid grid-cols-1 gap-4">
              <div>
                <h3 class="font-semibold mb-2">
                  Core
                </h3>

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

              <div>
                <h3 class="font-semibold mb-2">
                  Legacy Stack
                </h3>

                <div class="flex flex-wrap gap-2">
                  <span
                    v-for="skill in legacySkills"
                    :key="skill"
                    class="px-4 py-2 rounded-full bg-blue-50 border border-blue-100 text-sm"
                  >
                    {{ skill }}
                  </span>
                </div>
              </div>
            </div>
          </div>

        </div>

        <!-- Experience & Education -->
        <div class="flex flex-col gap-10">
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
                <ul class="list-disc list-outside ml-5 text-slate-700 space-y-1 mt-1">
                  <li>Collaborated with a team to develop a procurement and inventory management system.</li>
                  <li>Built a desktop application using VB.NET, SQL Server, and Crystal Reports.</li>
                  <li>Collaborated on system enhancements and bug fixes.</li>

                </ul>
              </div>

              <div>
                <h3 class="font-semibold">
                  Intern
                </h3>
                <p class="text-sm text-slate-500">2023–2024</p>
                <ul class="list-disc list-outside ml-5 text-slate-700 space-y-1 mt-1">
                  <li>Collaborated with a team to develop a field findings and promissory note management system.</li>
                  <li>Built a desktop application using VB.NET, SQL Server, and Crystal Reports.</li>
                  <li>Assisted in system enhancements and bug fixes.</li>
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
                  Sultan Kudarat State University · Graduated 2024
                </p>
              </div>

            </div>
          </div>
        </div>

      </div>

      <!-- Projects -->
      <div class="mb-12">
        <h2 class="uppercase font-semibold text-slate-600 mb-6">
          Featured Projects
        </h2>

        <div class="grid lg:grid-cols-3 gap-6">
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
const openToWork = true;

const skills = [
  'PHP',
  'Laravel',
  'JavaScript (ES6+)',
  'Vue.js',
  'Tailwind CSS',
  'REST APIs',
  'MySQL',
  'Git',
  'Composer', 
  'NPM',      
]

const legacySkills = [
  'VB.NET',
  'SQL Server',
  'SAP Crystal Reports',
]

const projects = [
  {
    title: 'ChatTayo',
    description:
      'Real-time messaging app with instant delivery, user presence, and persistent chat history. Built with Laravel Reverb (WebSockets) and Vue.js.',
    tags: ['Vue.js', 'Laravel', 'MySQL', 'Laravel Reverb', 'Laravel Echo', 'Tailwind CSS']
  },
  {
    title: 'Inventory Management System',
    description:
      'Inventory system with stock monitoring, purchase orders, and sales tracking. Includes Chart.js dashboards for inventory trends and status analytics.',
    tags: ['Vue.js', 'Laravel', 'MySQL', 'Chart.js', 'Tailwind CSS']
  },
  {
    title: 'ExpenseTracker',
    description:
      'Personal finance tracker built with custom MVC architecture. Features CRUD operations, category filtering, and monthly summary reports.',
    tags: ['PHP', 'JavaScript', 'MySQL', 'Tailwind CSS']
  }
]
</script>
