<template>
    <div class="lg:sticky lg:top-0 lg:flex lg:max-h-screen lg:w-1/2 lg:flex-col lg:justify-between lg:py-24">
        <div class="container  p-6 rounded-lg shadow-lg">
            <h1 class="text-3xl font-bold text-neutral-600 mb-4">Eviam Albuja</h1>
            <h2>Fullstack Developer</h2>
            <span class="text-base text-neutral-700">
                Meticulous and detail-oriented person, always focused on finding efficient
                and scalable solutions. I consider myself curious, resilient, and
                cheerful.
                <br />
                <br />
                Moreover, my experience as a competitive underwater hockey player has
                taught me the importance of discipline and teamwork, skills that I apply
                in my projects.
            </span>
            <nav>
                <ul class="mt-16">
                    <li>-- About</li>
                    <li>-- Projects</li>
                    <li>-- Skills</li>
                </ul>
            </nav>

        </div>
        <ul class="ml-1 mt-8 flex items-center">
            <li class="mr-5 shrink-0">
                <a href="" target="_blank" rel="noopener noreferrer">
                    <iconGitHub></iconGitHub>
                </a>
            </li>
            <li class="mr-5 shrink-0">
                <iconLinkedin></iconLinkedin>
            </li>
            <li class="mr-5 shrink-0">
                <iconResume></iconResume>
            </li>
        </ul>

    </div>
</template>

<script setup>
import iconGitHub from "./icons/github.vue"
import iconLinkedin from "./icons/linkedin.vue"
import iconResume from "./icons/resume.vue"
</script>

<style></style>