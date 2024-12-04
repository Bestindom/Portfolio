<template>
  <main class="pt-24 lg:w-1/2 lg:py-24">
    <section id="about" class="mb-16 scroll-mt-16 md:mb-24 lg:mb-36 lg:scroll-mt-24">
      <About />
    </section>
    <section id="experiencie" class="mb-16 scroll-mt-16 md:mb-24 lg:mb-36 lg:scroll-mt-24">
      <Experiencie />
    </section>
    <section id="projects" class="mb-16 scroll-mt-16 md:mb-24 lg:mb-36 lg:scroll-mt-24">
      <Projects />
    </section>
    <footer class="max-w-md pb-16 text-sm text-slate-500 sm:pb-0">
      <p>
        Built with
        <a href="https://vuejs.org/" target="_blank" rel="noreferrer noopener"
          class="font-medium text-slate-400 hover:text-teal-300 focus-visible:text-teal-300">VUE.js</a>
        and
        <a href="https://tailwindcss.com/" target="_blank" rel="noreferrer noopener"
          class="font-medium text-slate-400 hover:text-teal-300 focus-visible:text-teal-300">Tailwind CSS</a>,
        deployed with
        <a href="https://vercel.com/" target="_blank" rel="noreferrer noopener"
          class="font-medium text-slate-400 hover:text-teal-300 focus-visible:text-teal-300">Vercel</a>. All text is set
        in the Inter typeface.
      </p>
    </footer>
  </main>
</template>

<script setup>
import About from './sections/About.vue';
import Projects from './sections/Projects.vue';
import Experiencie from './sections/Experiencie.vue';
</script>
<style></style>
