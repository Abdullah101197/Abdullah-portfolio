<script setup>
import { portfolioData } from "../data/mockData";
const { skills } = portfolioData;

const skillCategories = [
    {
        name: "Frontend",
        items: skills.frontend,
        icon: "ph-fill ph-browser",
        color: "bg-blue-50 text-blue-600",
    },
    {
        name: "Backend",
        items: skills.backend,
        icon: "ph-fill ph-database",
        color: "bg-rose-50 text-rose-600",
    },
    {
        name: "Database",
        items: skills.database,
        icon: "ph-fill ph-hard-drives",
        color: "bg-emerald-50 text-emerald-600",
    },
    {
        name: "DevOps",
        items: skills.devops,
        icon: "ph-fill ph-gear",
        color: "bg-amber-50 text-amber-600",
    },
];
</script>

<template>
    <section
        id="skills"
        class="py-32 bg-white relative overflow-hidden bg-grain"
    >
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
            <div class="text-center mb-28">
                <div
                    class="inline-flex items-center space-x-2 px-3 py-1 rounded-full bg-emerald-50 border border-emerald-100 mb-8"
                >
                    <span
                        class="text-[10px] font-black text-emerald-700 uppercase tracking-[0.2em]"
                        >Tech Arsenal</span
                    >
                </div>
                <h2
                    class="text-5xl lg:text-7xl font-black font-display mb-8 tracking-tighter text-gray-900"
                >
                    Core Technologies
                </h2>
            </div>

            <div class="grid sm:grid-cols-2 lg:grid-cols-4 gap-6 lg:gap-8">
                <div
                    v-for="category in skillCategories"
                    :key="category.name"
                    class="bg-gray-50/50 rounded-[2.5rem] p-10 border border-transparent hover:border-emerald-100 hover:bg-white hover:shadow-[0_32px_64px_-16px_rgba(16,185,129,0.1)] transition-all duration-700 group"
                >
                    <div class="flex items-center mb-10">
                        <div
                            class="w-14 h-14 rounded-2xl flex items-center justify-center mr-5 shadow-sm group-hover:scale-110 group-hover:rotate-3 transition-all duration-700"
                            :class="category.color"
                        >
                            <i :class="[category.icon, 'text-2xl']"></i>
                        </div>
                        <h3
                            class="text-2xl font-black font-display tracking-tight text-gray-900"
                        >
                            {{ category.name }}
                        </h3>
                    </div>
                    <div class="space-y-3">
                        <div
                            v-for="item in category.items"
                            :key="item"
                            class="flex items-center px-4 py-3 bg-white/50 backdrop-blur-sm rounded-xl border border-gray-100/50 group/item hover:bg-emerald-50 hover:border-emerald-200 transition-all duration-300"
                        >
                            <div
                                class="w-1.5 h-1.5 rounded-full bg-emerald-500 mr-4 opacity-20 group-hover/item:opacity-100 group-hover/item:scale-125 transition-all"
                            ></div>
                            <span
                                class="font-bold text-gray-600 text-sm tracking-tight group-hover/item:text-emerald-900"
                            >
                                {{ item }}
                            </span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>
