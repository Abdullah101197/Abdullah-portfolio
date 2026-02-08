<script setup>
import { portfolioData } from "../data/mockData";
const { experience } = portfolioData;
</script>

<template>
    <section
        id="experience"
        class="py-32 bg-white relative overflow-hidden bg-grain"
    >
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
            <div class="text-center mb-28">
                <div
                    class="inline-flex items-center space-x-2 px-3 py-1 rounded-full bg-emerald-50 border border-emerald-100 mb-8"
                >
                    <span
                        class="text-[10px] font-black text-emerald-700 uppercase tracking-[0.2em]"
                        >Career Path</span
                    >
                </div>
                <h2
                    class="text-5xl lg:text-7xl font-black font-display mb-8 tracking-tighter text-gray-900"
                >
                    Professional Journey
                </h2>
                <p
                    class="text-xl text-gray-500 font-medium tracking-tight max-w-2xl mx-auto"
                >
                    A timeline of architectural contributions and leadership in
                    full-stack engineering.
                </p>
            </div>

            <div class="relative">
                <!-- Architectural Timeline Rail -->
                <div
                    class="absolute left-8 md:left-1/2 top-0 bottom-0 w-px bg-gradient-to-b from-transparent via-gray-200 to-transparent"
                ></div>

                <div class="space-y-24">
                    <div
                        v-for="(item, index) in experience"
                        :key="item.company"
                        class="relative flex items-center md:justify-center group"
                        :class="index % 2 !== 0 ? 'md:flex-row-reverse' : ''"
                    >
                        <!-- Timeline Node -->
                        <div
                            class="absolute left-8 md:left-1/2 w-4 h-4 bg-white rounded-full border-[3px] border-emerald-500 shadow-[0_0_20px_rgba(16,185,129,0.3)] transform -translate-x-2 z-10 transition-all duration-700 group-hover:scale-150 group-hover:bg-emerald-500"
                        ></div>

                        <div
                            class="ml-24 md:ml-0 md:w-5/12"
                            :class="
                                index % 2 === 0
                                    ? 'md:pr-20 md:text-right'
                                    : 'md:pl-20'
                            "
                        >
                            <div class="relative">
                                <span
                                    class="text-xs text-emerald-600 font-black uppercase tracking-[0.3em] mb-4 block"
                                >
                                    {{ item.period }}
                                </span>
                                <div
                                    class="bg-gray-50/50 rounded-[2rem] p-10 border border-transparent hover:border-emerald-100 hover:bg-white transition-all duration-700 hover:shadow-[0_32px_64px_-16px_rgba(0,0,0,0.05)] card-hover"
                                >
                                    <div
                                        class="flex items-center mb-6"
                                        :class="
                                            index % 2 === 0
                                                ? 'md:flex-row-reverse'
                                                : ''
                                        "
                                    >
                                        <div
                                            v-if="item.status"
                                            class="px-4 py-1 rounded-full bg-emerald-500 text-white text-[9px] font-black uppercase tracking-widest shadow-lg shadow-emerald-500/20"
                                            :class="
                                                index % 2 === 0
                                                    ? 'md:ml-4'
                                                    : 'mr-4'
                                            "
                                        >
                                            {{ item.status }}
                                        </div>
                                        <h3
                                            class="text-3xl font-black font-display tracking-tight text-gray-900 group-hover:text-emerald-600 transition-colors"
                                        >
                                            {{ item.role }}
                                        </h3>
                                    </div>
                                    <p
                                        class="text-emerald-700 font-black mb-8 tracking-widest text-xs uppercase opacity-60"
                                    >
                                        @ {{ item.company }}
                                    </p>
                                    <p
                                        class="text-gray-500 font-medium text-lg leading-relaxed tracking-tight"
                                    >
                                        {{ item.description }}
                                    </p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>
