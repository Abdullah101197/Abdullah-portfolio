<script setup>
import { portfolioData } from "../data/mockData";
const { projects, personalInfo } = portfolioData;
</script>

<template>
    <section id="projects" class="py-32 bg-gray-50/10 bg-grain">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div
                class="flex flex-col lg:flex-row justify-between items-end mb-28 gap-12"
            >
                <div class="max-w-3xl">
                    <div
                        class="inline-flex items-center space-x-2 px-3 py-1 rounded-full bg-emerald-50 border border-emerald-100 mb-8"
                    >
                        <span
                            class="text-[10px] font-black text-emerald-700 uppercase tracking-[0.2em]"
                            >Portfolio</span
                        >
                    </div>
                    <h2
                        class="text-6xl lg:text-[100px] font-black font-display mb-10 tracking-tighter text-gray-900 leading-[0.85]"
                    >
                        Selected <span class="text-gradient">Works</span>
                    </h2>
                    <p
                        class="text-xl text-gray-500 font-medium tracking-tight leading-relaxed"
                    >
                        A collection of architectural achievements, enterprise
                        solutions, and high-impact digital experiences.
                    </p>
                </div>
                <a
                    :href="personalInfo.github"
                    target="_blank"
                    class="group relative inline-flex items-center px-10 py-5 rounded-2xl bg-gray-950 text-white font-bold transition-all duration-300 hover:scale-105 active:scale-95 shadow-2xl shadow-gray-200 overflow-hidden"
                >
                    <div
                        class="absolute inset-0 bg-gradient-to-r from-emerald-500 to-teal-600 opacity-0 group-hover:opacity-10 transition-opacity"
                    ></div>
                    <i
                        class="ph-bold ph-github-logo mr-4 text-2xl group-hover:rotate-12 transition-transform"
                    ></i>
                    <span class="tracking-widest text-sm uppercase"
                        >Explore More</span
                    >
                </a>
            </div>

            <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-10 lg:gap-14">
                <div
                    v-for="project in projects"
                    :key="project.title"
                    class="group relative bg-white rounded-[3rem] overflow-hidden border border-gray-100 hover:border-emerald-200 transition-all duration-700 card-hover hover:shadow-[0_48px_80px_-16px_rgba(0,0,0,0.1)]"
                >
                    <div class="relative h-80 overflow-hidden">
                        <div
                            :class="[
                                'absolute inset-0 bg-gradient-to-br opacity-90 group-hover:scale-110 transition-transform duration-1000',
                                project.color,
                            ]"
                        ></div>
                        <div
                            class="absolute inset-0 flex items-center justify-center opacity-10 group-hover:opacity-20 transition-opacity duration-1000"
                        >
                            <i
                                :class="[
                                    project.icon,
                                    'text-[12rem] transform group-hover:rotate-12 group-hover:scale-125 transition-all duration-1000',
                                ]"
                            ></i>
                        </div>
                        <div
                            class="absolute inset-0 flex items-center justify-center p-12"
                        >
                            <div class="text-white text-center">
                                <span
                                    class="inline-block px-4 py-1.5 bg-white/10 backdrop-blur-md rounded-full text-[10px] font-black uppercase tracking-[0.2em] border border-white/20 mb-4 opacity-0 group-hover:opacity-100 transition-all translate-y-4 group-hover:translate-y-0 duration-500"
                                >
                                    {{ project.category }}
                                </span>
                                <h3
                                    class="text-3xl font-black font-display tracking-tight opacity-0 group-hover:opacity-100 transition-all translate-y-4 group-hover:translate-y-0 duration-500 delay-75"
                                >
                                    {{ project.title }}
                                </h3>
                            </div>
                        </div>
                    </div>

                    <div class="p-12">
                        <div class="flex justify-between items-start mb-6">
                            <h3
                                class="text-2xl font-black font-display tracking-tight text-gray-900 group-hover:text-emerald-600 transition-colors"
                            >
                                {{ project.title }}
                            </h3>
                            <i
                                class="ph ph-arrow-up-right text-gray-300 group-hover:text-emerald-500 group-hover:translate-x-1 group-hover:-translate-y-1 transition-all text-2xl"
                            ></i>
                        </div>
                        <p
                            class="text-gray-500 mb-10 text-lg font-medium leading-relaxed tracking-tight"
                        >
                            {{ project.description }}
                        </p>
                        <div class="flex flex-wrap gap-2">
                            <span
                                v-for="tag in project.tags"
                                :key="tag"
                                class="px-4 py-1.5 bg-gray-50/50 text-gray-600 rounded-xl text-[10px] font-black uppercase tracking-widest border border-gray-100 group-hover:bg-emerald-50 group-hover:text-emerald-700 group-hover:border-emerald-100 transition-all duration-500"
                            >
                                {{ tag }}
                            </span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>
