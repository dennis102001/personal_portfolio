<script setup>
</script>

<template>
  
  <div class="min-h-screen bg-white md:bg-slate-50 pt-26 pb-10 sm:px-4 md:px-6 md:pt-32 md:pb-6">
    <div
      class="max-w-6xl mx-auto bg-white rounded-[2rem] md:shadow-xl p-8 md:p-10"
    >      
      <!-- Hero -->
      <section id="hero" class="scroll-mt-28 flex flex-col md:flex-row md:items-center md:justify-between gap-6 mb-10">
        <div>
          <h1 class="text-4xl md:text-5xl font-bold bg-gradient-to-r from-slate-900 to-blue-900 bg-clip-text text-transparent">
            Dennis Bedaña
          </h1>

          <div class="inline-block mt-3 px-4 py-1 rounded-full bg-blue-50 border border-blue-100 text-slate-700 text-sm font-semibold">
            <i class="fa-solid fa-code mr-2 text-blue-950"></i>
            Junior Full-Stack Web Developer
          </div>

          <p class="mt-4 max-w-lg text-slate-700">
            Junior Full-Stack Developer building modern, user-friendly web applications with Laravel and Vue.js.
          </p>
        </div>

        <div class="flex w-fit items-center gap-3 px-6 py-3 rounded-full bg-blue-50 border border-blue-100 text-slate-800">
          <div v-if="openToWork">
            <i class="fa-solid fa-map-pin mr-1 text-xl text-blue-950"></i>
            Remote · Open to Work
          </div>

          <div v-else>
            <i class="fa-solid fa-map-pin mr-1 text-xl text-blue-950"></i>
            Philippines · Junior Full-Stack Developer
          </div>
        </div>
      </section>

      <!-- Contact -->
      <section id="contact" class="scroll-mt-28 flex flex-wrap gap-6 pb-8 mb-10 border-b border-slate-200 text-sm">
        <a href="mailto:dennisbed1001@gmail.com" class="link" title="Send me an email">
          <i class="fa-solid fa-envelope mr-1 text-blue-950"></i>
          dennisbed1001@gmail.com
        </a>

        <a href="https://github.com/dennis102001" target="_blank" rel="noopener noreferrer" class="link" title="GitHub">
          <i class="fa-brands fa-github mr-1 text-blue-950"></i>
          github.com/dennis102001
        </a>

        <a href="tel:+639513754423" class="link" title="Call or text me">
          <i class="fa-solid fa-phone-flip mr-1 text-blue-950"></i>
          +63 9513754423
        </a>

        <a href="resume/Dennis_Bedana_Resume.pdf" target="_blank" rel="noopener noreferrer" class="link" title="Download my resume (PDF)">
            <i class="fas fa-file text-sm mr-1 text-blue-950"></i>
            Resume
          </a>
      </section>

      <div class="grid md:grid-cols-2 gap-10 mb-12">
        <!-- About & Skills -->
        <section id="about" class="scroll-mt-28 flex flex-col gap-10">

          <div>
            <h2 class="uppercase font-semibold text-slate-600 mb-4">
              <i class="fa-solid fa-user-astronaut mr-1 text-blue-950"></i>
              About
            </h2>

            <p class="text-slate-700 mb-4">
              Hi, I'm Dennis, a Junior Full-Stack Web Developer passionate about building clean, functional, 
              and user-friendly web applications. I transitioned from desktop development with 
              <span class="highlight">VB.NET</span> and <span class="highlight">SQL Server</span>
              to modern web technologies, focusing on <span class="highlight">Laravel</span>, 
              <span class="highlight">Vue.js</span>, and <span class="highlight">Tailwind CSS</span>.
            </p>

            <p class="text-slate-700">
              I continuously improve my skills by building personal projects and learning new technologies.
              I'm currently open to opportunities where I can grow as a developer and contribute to meaningful projects.
            </p>
          </div>

          <div>
            <h2 class="uppercase font-semibold text-slate-600 mb-4">
              <i class="fa-solid fa-laptop-code mr-1 text-blue-950"></i>
              Tech stack
            </h2>

            <div class="grid grid-cols-1 gap-4">
              <div>
                <h3 class="font-semibold text-slate-900 mb-2">
                  Core
                </h3>

                <div class="flex flex-wrap gap-2">
                  <span
                    v-for="skill in skills"
                    :key="skill"
                    class="px-4 py-2 rounded-full bg-blue-50 border border-blue-100 text-sm text-slate-700"
                  >
                    {{ skill }}
                  </span>
                </div>
              </div>

              <div>
                <h3 class="font-semibold text-slate-900 mb-2">
                  Legacy Stack
                </h3>

                <div class="flex flex-wrap gap-2">
                  <span
                    v-for="skill in legacySkills"
                    :key="skill"
                    class="px-4 py-2 rounded-full bg-blue-50 border border-blue-100 text-sm text-slate-700"
                  >
                    {{ skill }}
                  </span>
                </div>
              </div>
            </div>
          </div>

        </section>

        <!-- Experiences, Education, & Certifications -->
        <section id="experience" class="scroll-mt-28 flex flex-col gap-10">
          <div>
            <h2 class="uppercase font-semibold text-slate-600 mb-4">
              <i class="fa-solid fa-briefcase mr-1 text-blue-950"></i>
              Experience
            </h2>

            <div class="space-y-4">
              <div>
                <h3 class="font-semibold text-slate-900">
                  Computer Programmer · 
                  <span class="font-normal">Part-time </span>
                  <span class="font-normal text-slate-500">(2024–2025)</span>
                </h3>
                <p class="text-slate-700">
                  Contributed to the development of a procurement and inventory management system using VB.NET, SQL Server, and Crystal Reports. 
                  Assisted with feature enhancements and bug fixes.
                </p>
              </div>

              <div>
                <h3 class="font-semibold text-slate-900">
                  On-the-Job Trainee <span class="font-normal text-slate-500">(2023–2024)</span>
                </h3>
                <p class="text-slate-700">
                  Collaborated on the development of a field findings and promissory note management system using VB.NET, SQL Server, 
                  and Crystal Reports. Supported system enhancements and bug fixes.
                </p>
              </div>
            </div>
          </div>

          <div>
            <h2 class="uppercase font-semibold text-slate-600 mb-4">
              <i class="fa-solid fa-graduation-cap mr-1 text-blue-950"></i>
              Education
            </h2>

            <div class="space-y-4">
              <div>
                <h3 class="font-semibold text-slate-900">
                  B.S. Information Technology
                </h3>
                <p class="text-slate-500">
                  Sultan Kudarat State University · Graduated 2024
                </p>
              </div>

            </div>
          </div>

          <!-- Certifications -->
          <div>
            <h2 class="uppercase font-semibold text-slate-600 mb-4">
              <i class="fa-solid fa-id-card mr-1 text-blue-950"></i>
              Certifications & Eligibility
            </h2>

            <div class="p-5 rounded-2xl border border-slate-200 bg-slate-50">
              <h3 class="font-semibold text-slate-900">
                Civil Service Professional Eligibility
              </h3>

              <p class="text-sm text-slate-500 mt-1">
                Civil Service Commission, Philippines · 2025
              </p>
            </div>
          </div>
        </section>

      </div>

      <!-- Projects -->
      <section id="projects" class="mb-12 scroll-mt-28">
        <h2 class="uppercase font-semibold text-slate-600 mb-6">
          <i class="fa-solid fa-folder-open mr-1 text-blue-950"></i>
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
                class="px-3 py-1 rounded-full bg-blue-100 text-xs font-semibold text-slate-700"
              >
                {{ tag }}
              </span>
            </div>

            <div class="flex gap-4 text-sm text-blue-900">
              <a :href="project.link" target="_blank" rel="noopener noreferrer" class="link">
                <i class="fa-brands fa-github mr-1 text-blue-950"></i>
                Code
              </a>

              <a href="#" class="link">
                <i class="fa-solid fa-globe mr-1 text-blue-950"></i>
                Demo
              </a>
            </div>
          </div>
        </div>
      </section>

      <!-- Footer -->
      <div class="mt-12 pt-8 border-t border-slate-200 flex flex-col sm:flex-row justify-between gap-4 text-slate-500">
        <div class="flex flex-col items-center sm:items-start">
          <div class="flex flex-row items-center">
            <i class="fa-regular fa-copyright text-xs mr-1 mt-[2px] text-blue-950"></i>
            <p class="text-slate-700">2026 · Dennis Bedaña</p>
          </div>
          <div class="flex flex-row items-center">
            <i class="fa-solid fa-code text-xs mr-2 text-blue-950"></i>
            <p class="text-xs">Built with Vue.js and Tailwind CSS</p>
          </div>
        </div>
        
        <div class="flex gap-3 justify-center">
          <a href="mailto:dennisbed1001@gmail.com" class="icon-link" title="Send me an email">
            <i class="fa-solid fa-envelope text-sm"></i>
          </a>
          <a href="https://github.com/dennis102001" target="_blank" rel="noopener noreferrer" class="icon-link" title="GitHub">
            <i class="fa-brands fa-github text-sm"></i>
          </a>
          <a href="tel:+639513754423" class="icon-link" title="Call or text me">
            <i class="fa-solid fa-phone-flip text-sm"></i>
          </a>
          <a href="/resume/Dennis_Bedana_Resume.pdf" target="_blank" rel="noopener noreferrer" class="icon-link" title="Download my resume (PDF)">
            <i class="fas fa-file text-sm"></i>
          </a>
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
    tags: ['Vue.js', 'Laravel', 'MySQL', 'Laravel Reverb', 'Laravel Echo', 'Tailwind CSS'],
    link: "https://github.com/dennis102001/chat-tayo"
  },
  {
    title: 'Inventory Management System',
    description:
      'Inventory system with stock monitoring, purchase orders, and sales tracking. Includes Chart.js dashboards for inventory trends and status analytics.',
    tags: ['Vue.js', 'Laravel', 'MySQL', 'Chart.js', 'Tailwind CSS'],
    link: "https://github.com/dennis102001/simple_ims_spa"
  },
  {
    title: 'Expense Tracker',
    description:
      'Personal finance tracker built with custom MVC architecture. Features CRUD operations, category filtering, and monthly summary reports.',
    tags: ['PHP', 'JavaScript', 'MySQL', 'Tailwind CSS'],
    link: "https://github.com/dennis102001/expense_app"
  }
]
</script>
