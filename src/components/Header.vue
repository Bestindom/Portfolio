<template>
    <header class="lg:sticky lg:top-0 lg:flex lg:max-h-screen lg:w-1/2 lg:flex-col lg:justify-between lg:py-24">
        <div>
            <h1 class="text-4xl font-bold tracking-tight text-slate-200 sm:text-5xl">
                <a href="/">Eviam Albuja</a>
            </h1>
            <h2 class="mt-3 text-lg font-medium tracking-tight text-slate-200 sm:text-xl">Fullstack Developer</h2>
            <p class="mt-4 max-w-xs leading-normal">
                Innate thinker focused on efficiency.
            </p>
            <nav class="nav hidden lg:block">
                <ul class="mt-16 w-max">
                    <li>
                        <a class="group flex items-center py-3" href="#about">
                            <span
                                class="nav-indicator mr-4 h-px  transition-all group-hover:w-16 group-hover:bg-slate-200 group-focus-visible:w-16 group-focus-visible:bg-slate-200"
                                :class="{
                                    'w-16 bg-slate-200': activeSection === 'about',
                                    'w-8 bg-slate-600': activeSection !== 'about'
                                }"></span>
                            <span class="nav-text text-xs font-bold uppercase tracking-wides group-hover:text-slate-200"
                                :class="{
                                    'text-slate-200': activeSection === 'about',
                                    'text-slate-500': activeSection !== 'about'
                                }">
                                about
                            </span>
                        </a>
                    </li>
                    <li>
                        <a class="group flex items-center py-3" href="#experiencie">
                            <span
                                class="nav-indicator mr-4 h-px transition-all group-hover:w-16 group-hover:bg-slate-200 group-focus-visible:w-16 group-focus-visible:bg-slate-200"
                                :class="{
                                    'w-16 bg-slate-200': activeSection === 'experiencie',
                                    'w-8 bg-slate-600': activeSection !== 'experiencie'
                                }"></span>
                            <span
                                class="nav-text text-xs font-bold uppercase tracking-widest group-hover:text-slate-200"
                                :class="{
                                    'text-slate-200': activeSection === 'experiencie',
                                    'text-slate-500': activeSection !== 'experiencie'
                                }">
                                experiencie
                            </span>
                        </a>
                    </li>
                    <li>
                        <a class="group flex items-center py-3" href="#projects">
                            <span
                                class="nav-indicator mr-4 h-px transition-all group-hover:w-16 group-hover:bg-slate-200 group-focus-visible:w-16 group-focus-visible:bg-slate-200"
                                :class="{
                                    'w-16 bg-slate-200': activeSection === 'projects',
                                    'w-8 bg-slate-600': activeSection !== 'projects'
                                }"></span>
                            <span
                                class="nav-text text-xs font-bold uppercase tracking-widest group-hover:text-slate-200"
                                :class="{
                                    'text-slate-200': activeSection === 'projects',
                                    'text-slate-500': activeSection !== 'projects'
                                }">
                                projects
                            </span>
                        </a>
                    </li>
                </ul>
            </nav>

        </div>
        <ul class="ml-1 mt-8 flex items-center">
            <li class="mr-5 shrink-0">
                <a href="https://github.com/Bestindom" target="_blank" rel="noopener noreferrer">
                    <iconGitHub></iconGitHub>
                </a>
            </li>
            <li class="mr-5 shrink-0">
                <a href="https://www.linkedin.com/in/eviamalbuja/" target="_blank" rel="noopener noreferrer">
                    <iconLinkedin></iconLinkedin>
                </a>
            </li>
            <li class="mr-5 shrink-0">
                <a href="./static/CV_2025_ENG.pdf" target="_blank" rel="noopener noreferrer">
                    <iconResume></iconResume>
                </a>
            </li>
        </ul>

    </header>
</template>

<script setup>
import iconGitHub from "./icons/github.vue"
import iconLinkedin from "./icons/linkedin.vue"
import iconResume from "./icons/resume.vue"

import { ref, onMounted, onUnmounted } from "vue";

const activeSection = ref("about");

const handleScroll = () => {
    const sections = document.querySelectorAll("section");
    let currentSection = "";

    sections.forEach((section) => {
        const rect = section.getBoundingClientRect();
        if (rect.top < window.innerHeight / 2 && rect.bottom > window.innerHeight / 2) {
            currentSection = section.id; // update active section
        }
    });

    activeSection.value = currentSection;
};

onMounted(() => {
    window.addEventListener("scroll", handleScroll);
});

onUnmounted(() => {
    window.removeEventListener("scroll", handleScroll);
});
</script>

<style></style>