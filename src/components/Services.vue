<script setup>
import { portfolioData } from "../data/mockData";
const { services } = portfolioData;
</script>

<template>
    <section
        id="services"
        class="py-32 bg-gray-50/30 relative overflow-hidden bg-grain"
    >
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
            <div class="text-center mb-28">
                <div
                    class="inline-flex items-center space-x-2 px-3 py-1 rounded-full bg-emerald-50 border border-emerald-100 mb-8"
                >
                    <div
                        class="w-1.5 h-1.5 rounded-full bg-emerald-500 animate-pulse"
                    ></div>
                    <span
                        class="text-[10px] font-black text-emerald-700 uppercase tracking-[0.2em]"
                        >Expertise</span
                    >
                </div>
                <h2
                    class="text-5xl lg:text-7xl font-black font-display mb-8 tracking-tighter text-gray-900"
                >
                    Premium Solutions
                </h2>
                <p
                    class="text-xl text-gray-500 max-w-2xl mx-auto font-medium tracking-tight leading-relaxed"
                >
                    Engineering scalable architectures and high-performance
                    applications designed for modern business needs.
                </p>
            </div>

            <div class="grid md:grid-cols-3 gap-8 lg:gap-12">
                <div
                    v-for="service in services"
                    :key="service.title"
                    class="group relative bg-white rounded-[2.5rem] p-12 transition-all duration-700 border border-gray-100 hover:border-emerald-200 hover:shadow-[0_40px_80px_-20px_rgba(0,0,0,0.06)] card-hover"
                >
                    <div class="relative z-10">
                        <div
                            class="w-20 h-20 rounded-3xl flex items-center justify-center mb-12 shadow-sm transition-all duration-700 group-hover:scale-110 group-hover:rotate-3 group-hover:shadow-emerald-200/50"
                            :class="
                                service.variant === 'highlight'
                                    ? 'bg-emerald-500 shadow-emerald-500/20'
                                    : 'bg-gray-50 shadow-gray-200/50'
                            "
                        >
                            <i
                                :class="[
                                    service.icon,
                                    'text-4xl',
                                    service.variant === 'highlight'
                                        ? 'text-white'
                                        : 'text-emerald-500',
                                ]"
                            ></i>
                        </div>
                        <h3
                            class="text-3xl font-black mb-6 font-display tracking-tight text-gray-900 group-hover:text-emerald-600 transition-colors"
                        >
                            {{ service.title }}
                        </h3>
                        <p
                            class="text-gray-500 mb-12 leading-relaxed font-medium tracking-tight text-lg"
                        >
                            {{ service.description }}
                        </p>
                        <ul class="space-y-5">
                            <li
                                v-for="feature in service.features"
                                :key="feature"
                                class="flex items-center font-bold text-sm tracking-tight text-gray-700 group/item"
                            >
                                <div
                                    class="w-2 h-2 rounded-full bg-emerald-500/20 mr-4 group-hover/item:bg-emerald-500 group-hover/item:scale-125 transition-all"
                                ></div>
                                <span>{{ feature }}</span>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>
