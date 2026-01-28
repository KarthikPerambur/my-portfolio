<script setup>
import coverPic from './assets/cover_pic.jpeg'
import resumePdf from './assets/resume.pdf'
</script>

<template>
  <div class="min-h-screen bg-slate-50">
    <!-- Hero Section -->
    <section class="relative py-12 sm:py-16 md:py-20 lg:py-28 overflow-hidden">
      <!-- Background Image -->
      <div 
        class="absolute inset-0 bg-cover bg-center bg-no-repeat opacity-20" 
        :style="{ backgroundImage: `url(${coverPic})` }"
      ></div>
      <!-- Overlay to ensure text readability -->
      <div class="absolute inset-0 bg-slate-50/60"></div>
      <!-- Content -->
      <div class="relative z-10 max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
        <!-- Name/Title -->
        <h1 class="text-3xl sm:text-4xl md:text-5xl lg:text-6xl font-bold tracking-tight text-slate-900">
          Skandha's Dad 
          <span class="block sm:inline text-blue-600 mt-1 sm:mt-0">(Karthik Rammoorthy)</span>
        </h1>
        
        <!-- Bio -->
        <p class="mt-4 sm:mt-6 text-base sm:text-lg md:text-xl text-slate-600 max-w-2xl leading-relaxed">
          Senior Software Engineer specializing in <span class="text-slate-900 font-semibold">scalable and responsive applications</span>. 
          <br class="hidden md:block" />
          Currently working at Benevity, building secure identity platforms and resilient applications.
        </p>
        
        <!-- Contact Links - Stack on mobile, inline on larger screens -->
        <div class="mt-6 sm:mt-8 flex flex-col sm:flex-row sm:flex-wrap sm:items-center gap-3 sm:gap-4">
          <div class="flex flex-wrap items-center gap-3 sm:gap-4">
            <a 
              href="https://www.linkedin.com/in/karthik-rammoorthy/" 
              target="_blank"
              rel="noopener noreferrer"
              class="text-sm font-medium text-slate-700 hover:text-blue-600 active:text-blue-700 transition py-1"
            >
              LinkedIn
            </a>
            <a 
              href="mailto:rkarthikkumar@outlook.com"
              class="text-sm font-medium text-slate-700 hover:text-blue-600 active:text-blue-700 transition py-1"
            >
              Email
            </a>
            <a 
              href="tel:+16479061953" 
              class="text-sm font-medium text-slate-700 hover:text-blue-600 active:text-blue-700 transition py-1"
            >
              Phone
            </a>
          </div>
          <span class="hidden sm:inline text-gray-300">|</span>
          <span class="text-sm text-gray-500">Based in Ontario, CA</span>
        </div>

        <!-- Resume Download Button -->
        <div class="mt-6 sm:mt-8">
          <a 
            :href="resumePdf" 
            download="Karthik_Rammoorthy_Resume.pdf"
            class="inline-flex items-center justify-center gap-2 w-full sm:w-auto px-5 py-3 sm:py-2.5 bg-blue-600 text-white text-sm font-medium rounded-lg hover:bg-blue-700 active:bg-blue-800 transition shadow-sm hover:shadow-md"
          >
            <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
              <path stroke-linecap="round" stroke-linejoin="round" d="M12 10v6m0 0l-3-3m3 3l3-3m2 8H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z" />
            </svg>
            Download Resume
          </a>
        </div>
      </div>
    </section>

    <!-- Case Studies Container -->
    <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 pb-12 sm:pb-16 lg:pb-24">
      
      <!-- Case Study 1: Identity & Auth Module -->
      <section class="mb-12 sm:mb-16 lg:mb-20">
        <h2 class="text-xs font-bold uppercase tracking-widest text-slate-500 mb-6 sm:mb-8">Case Study 01</h2>
        
        <div class="group relative grid gap-3 sm:gap-4 transition-all md:grid-cols-8 md:gap-8 lg:gap-10 hover:bg-white/70 p-4 sm:p-6 rounded-xl border border-slate-100 sm:border-transparent hover:border-slate-200 hover:shadow-sm -mx-4 sm:-mx-6 bg-white/40 sm:bg-transparent">
          <div class="md:col-span-2 text-sm font-semibold text-slate-400 order-first">2023 — 2025</div>
          <div class="md:col-span-6">
            <h3 class="text-lg sm:text-xl font-bold text-slate-900 group-hover:text-blue-600 transition">
              Ecosystem-Wide Identity & Auth Module
            </h3>
            
            <!-- Problem -->
            <div class="mt-3 sm:mt-4">
              <h4 class="text-xs font-semibold uppercase tracking-wide text-slate-500">Problem</h4>
              <p class="mt-1 text-sm sm:text-base text-slate-600 leading-relaxed">
                Benevity's ecosystem had fragmented authentication across multiple applications, leading to inconsistent user experiences, security vulnerabilities, and high maintenance overhead. The system also struggled to handle traffic spikes during peak giving events.
              </p>
            </div>
            
            <!-- Solution -->
            <div class="mt-3 sm:mt-4">
              <h4 class="text-xs font-semibold uppercase tracking-wide text-slate-500">Solution</h4>
              <p class="mt-1 text-sm sm:text-base text-slate-600 leading-relaxed">
                Developed a centralized Vue 3 authentication UI module integrated with Auth0, providing a unified login experience across the entire company ecosystem. Built with TypeScript for type safety. On the backend, implemented Spring Boot microservices to securely handle and store PII data, backed by CockroachDB for distributed, resilient data persistence. Deployed the entire solution on AWS infrastructure for scalability and high availability.
              </p>
            </div>
            
            <!-- Impact -->
            <div class="mt-3 sm:mt-4">
              <h4 class="text-xs font-semibold uppercase tracking-wide text-slate-500">Impact</h4>
              <p class="mt-1 text-sm sm:text-base text-slate-600 leading-relaxed">
                Successfully handled 10x traffic spikes during Giving Tuesday with zero downtime. Reduced authentication-related bugs by consolidating security protocols, and improved developer velocity by eliminating duplicate auth implementations across teams.
              </p>
            </div>
            
            <ul class="mt-4 sm:mt-5 flex flex-wrap gap-2">
              <li class="px-2.5 sm:px-3 py-1 bg-blue-50 text-blue-700 text-xs font-medium rounded-full">Vue 3</li>
              <li class="px-2.5 sm:px-3 py-1 bg-blue-50 text-blue-700 text-xs font-medium rounded-full">TypeScript</li>
              <li class="px-2.5 sm:px-3 py-1 bg-blue-50 text-blue-700 text-xs font-medium rounded-full">Auth0</li>
              <li class="px-2.5 sm:px-3 py-1 bg-blue-50 text-blue-700 text-xs font-medium rounded-full">Spring Boot</li>
              <li class="px-2.5 sm:px-3 py-1 bg-blue-50 text-blue-700 text-xs font-medium rounded-full">CockroachDB</li>
              <li class="px-2.5 sm:px-3 py-1 bg-blue-50 text-blue-700 text-xs font-medium rounded-full">AWS</li>
            </ul>
          </div>
        </div>
      </section>

      <!-- Case Study 2: Volunteering Services Platform -->
      <section>
        <h2 class="text-xs font-bold uppercase tracking-widest text-slate-500 mb-6 sm:mb-8">Case Study 02</h2>
        
        <div class="group relative grid gap-3 sm:gap-4 transition-all md:grid-cols-8 md:gap-8 lg:gap-10 hover:bg-white/70 p-4 sm:p-6 rounded-xl border border-slate-100 sm:border-transparent hover:border-slate-200 hover:shadow-sm -mx-4 sm:-mx-6 bg-white/40 sm:bg-transparent">
          <div class="md:col-span-2 text-sm font-semibold text-slate-400 order-first">2022 — 2024</div>
          <div class="md:col-span-6">
            <h3 class="text-lg sm:text-xl font-bold text-slate-900 group-hover:text-blue-600 transition">
              Volunteering Services Platform
            </h3>
            
            <!-- Problem -->
            <div class="mt-3 sm:mt-4">
              <h4 class="text-xs font-semibold uppercase tracking-wide text-slate-500">Problem</h4>
              <p class="mt-1 text-sm sm:text-base text-slate-600 leading-relaxed">
                Corporate volunteering programs struggled with clunky interfaces that made it difficult for employees to discover opportunities, track hours, and stay engaged. Low participation rates and poor user experience were hurting program adoption.
              </p>
            </div>
            
            <!-- Solution -->
            <div class="mt-3 sm:mt-4">
              <h4 class="text-xs font-semibold uppercase tracking-wide text-slate-500">Solution</h4>
              <p class="mt-1 text-sm sm:text-base text-slate-600 leading-relaxed">
                Built a modern, intuitive Vue 3 volunteering platform with a focus on delightful user experience. Implemented smooth animations and micro-interactions using CSS transitions and Vue's Transition API. Designed responsive layouts using PrimeVue's rich component library, built custom themed components, and optimized performance with lazy loading and virtual scrolling for large opportunity lists. Integrated interactive maps, real-time search filtering, and an accessible design system following WCAG guidelines.
              </p>
            </div>
            
            <!-- Impact -->
            <div class="mt-3 sm:mt-4">
              <h4 class="text-xs font-semibold uppercase tracking-wide text-slate-500">Impact</h4>
              <p class="mt-1 text-sm sm:text-base text-slate-600 leading-relaxed">
                Increased volunteer sign-up rates by 40% through improved UX. Achieved 95+ Lighthouse performance scores across all pages. Reduced page load times by 60% with code splitting and optimized asset delivery. The platform now serves thousands of employees discovering and participating in volunteer opportunities.
              </p>
            </div>
            
            <ul class="mt-4 sm:mt-5 flex flex-wrap gap-2">
              <li class="px-2.5 sm:px-3 py-1 bg-blue-50 text-blue-700 text-xs font-medium rounded-full">Vue 3</li>
              <li class="px-2.5 sm:px-3 py-1 bg-blue-50 text-blue-700 text-xs font-medium rounded-full">TypeScript</li>
              <li class="px-2.5 sm:px-3 py-1 bg-blue-50 text-blue-700 text-xs font-medium rounded-full">PrimeVue</li>
              <li class="px-2.5 sm:px-3 py-1 bg-blue-50 text-blue-700 text-xs font-medium rounded-full">Pinia</li>
              <li class="px-2.5 sm:px-3 py-1 bg-blue-50 text-blue-700 text-xs font-medium rounded-full">Vite</li>
              <li class="px-2.5 sm:px-3 py-1 bg-blue-50 text-blue-700 text-xs font-medium rounded-full">Accessibility</li>
            </ul>
          </div>
        </div>
      </section>

    </div>
  </div>
</template>