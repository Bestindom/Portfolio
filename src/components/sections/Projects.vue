<template>
    <div>
        <ul class="group/list">
            <li v-for="project in projects" :key="project.name" class="mb-12">
                <div
                    class="group relative grid gap-4 pb-1 transition-all sm:grid-cols-8 sm:gap-8 md:gap-4 lg:hover:!opacity-100 lg:group-hover/list:opacity-50">
                    <div
                        class="absolute -inset-x-4 -inset-y-4 z-0 hidden rounded-md transition motion-reduce:transition-none lg:-inset-x-6 lg:block lg:group-hover:bg-slate-800/50 lg:group-hover:shadow-[inset_0_1px_0_0_rgba(148,163,184,0.1)] lg:group-hover:drop-shadow-lg">
                    </div>
                    <div class="z-10 sm:order-2 sm:col-span-6">
                        <h3>
                            <a class="inline-flex items-baseline font-medium leading-tight text-slate-200 hover:text-teal-300 focus-visible:text-teal-300  group/link text-base"
                                :href="project.url" target="_blank" rel="noreferrer noopener">
                                <span class="absolute -inset-x-4 -inset-y-2.5 hidden rounded md:-inset-x-6 md:-inset-y-4 lg:block">

                                </span>
                                <span>{{ project.name }}</span>
                            </a>
                        </h3>
                        <p class="mt-2 text-sm leading-normal">{{ project.description }}</p>
                    </div>
                    <img :src="project.img" alt="" class="aspect-video object-cover rounded border-2 border-slate-200/10 transition group-hover:border-slate-200/30 sm:order-1 sm:col-span-2 sm:translate-y-1">
                </div>
            </li>
        </ul>
    </div>
</template>
<script setup>
import projects from "@/content/projects.json"
</script>
<style></style>