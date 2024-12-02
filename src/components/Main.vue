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
  </main>
</template>

<script setup>
import About from './sections/About.vue';
import Projects from './sections/Projects.vue';
import Experiencie from './sections/Experiencie.vue';
</script>
<style></style>
