<script setup>
import { portfolioData } from "../data/mockData";
const { personalInfo } = portfolioData;
</script>

<template>
    <section
        id="home"
        class="relative min-h-[95vh] flex items-center justify-center overflow-hidden bg-white selection:bg-emerald-100 selection:text-emerald-900"
    >
        <!-- Sophisticated Mesh Gradient Background -->
        <div class="absolute inset-0 z-0">
            <div
                class="absolute top-[-10%] right-[-10%] w-[1000px] h-[1000px] bg-emerald-50/50 rounded-full blur-[160px] animate-float opacity-40 hover:opacity-60 transition-opacity duration-1000"
            ></div>
            <div
                class="absolute bottom-[-10%] left-[-10%] w-[800px] h-[800px] bg-teal-50/50 rounded-full blur-[160px] opacity-40 hover:opacity-60 transition-opacity duration-1000"
                style="animation: float 12s ease-in-out infinite reverse"
            ></div>
            <div
                class="absolute inset-0 bg-[radial-gradient(#e5e7eb_1px,transparent_1px)] [background-size:40px_40px] [mask-image:radial-gradient(ellipse_50%_50%_at_50%_50%,#000_70%,transparent_100%)] opacity-20"
            ></div>
        </div>

        <div class="relative z-10 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-32">
            <div class="grid lg:grid-cols-2 gap-20 items-center">
                <div class="text-center lg:text-left">
                    <div
                        class="inline-flex items-center space-x-2 px-4 py-2 rounded-full bg-white/80 backdrop-blur-sm shadow-xl shadow-gray-100 border border-emerald-50 mb-10 card-hover"
                    >
                        <span class="relative flex h-3 w-3">
                            <span
                                class="animate-ping absolute inline-flex h-full w-full rounded-full bg-emerald-400 opacity-75"
                            ></span>
                            <span
                                class="relative inline-flex rounded-full h-3 w-3 bg-emerald-500"
                            ></span>
                        </span>
                        <span
                            class="text-[10px] font-black text-gray-500 uppercase tracking-[0.2em]"
                            >Available for Hire</span
                        >
                    </div>

                    <h1
                        class="text-6xl sm:text-7xl lg:text-[100px] font-black font-display leading-[0.85] mb-8 tracking-tighter text-gray-900"
                    >
                        {{
                            personalInfo.tagline
                                .split(" ")
                                .slice(0, 2)
                                .join(" ")
                        }}
                        <span
                            class="block text-gradient mt-2 leading-none pb-2"
                            >{{
                                personalInfo.tagline
                                    .split(" ")
                                    .slice(2)
                                    .join(" ")
                            }}</span
                        >
                    </h1>

                    <p
                        class="text-xl text-gray-500 mb-12 leading-relaxed max-w-xl mx-auto lg:mx-0 font-medium tracking-tight"
                    >
                        {{ personalInfo.description }}
                    </p>

                    <div
                        class="flex flex-col sm:flex-row gap-5 justify-center lg:justify-start mb-20"
                    >
                        <a
                            :href="personalInfo.whatsapp"
                            target="_blank"
                            class="group relative inline-flex items-center justify-center px-10 py-5 rounded-2xl bg-emerald-500 text-white font-bold shadow-2xl shadow-emerald-500/30 hover:shadow-emerald-500/50 transition-all duration-300 hover:scale-105 active:scale-95"
                        >
                            <i
                                class="ph-fill ph-whatsapp-logo text-2xl mr-3 group-hover:rotate-12 transition-transform"
                            ></i>
                            <span class="text-lg">WhatsApp Me</span>
                        </a>
                        <a
                            href="#projects"
                            class="group inline-flex items-center justify-center px-10 py-5 rounded-2xl bg-white text-gray-900 font-bold border-2 border-gray-100 hover:border-emerald-500 hover:text-emerald-600 transition-all duration-300 hover:scale-105 active:scale-95 shadow-xl shadow-gray-100/50"
                        >
                            <span class="text-lg">View My Work</span>
                            <i
                                class="ph-bold ph-arrow-down ml-3 group-hover:translate-y-1 transition-transform"
                            ></i>
                        </a>
                    </div>

                    <div
                        class="flex flex-wrap items-center justify-center lg:justify-start gap-x-12 gap-y-8 max-w-lg mx-auto lg:mx-0"
                    >
                        <div class="group">
                            <div
                                class="text-5xl font-black text-gray-900 tracking-tighter group-hover:text-emerald-500 transition-colors"
                            >
                                {{ personalInfo.experience }}
                            </div>
                            <div
                                class="text-[10px] font-bold text-gray-400 uppercase tracking-widest mt-1"
                            >
                                Experience
                            </div>
                        </div>
                        <div class="group">
                            <div
                                class="text-5xl font-black text-gray-900 tracking-tighter group-hover:text-emerald-500 transition-colors"
                            >
                                30+
                            </div>
                            <div
                                class="text-[10px] font-bold text-gray-400 uppercase tracking-widest mt-1"
                            >
                                Projects
                            </div>
                        </div>
                        <div class="group">
                            <div
                                class="text-5xl font-black text-gray-900 tracking-tighter group-hover:text-emerald-500 transition-colors"
                            >
                                100%
                            </div>
                            <div
                                class="text-[10px] font-bold text-gray-400 uppercase tracking-widest mt-1"
                            >
                                Success
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Premium Code Snippet Visualization -->
                <div class="relative hidden lg:block perspective-1000">
                    <div class="relative group animate-float translate-z-10">
                        <div
                            class="absolute inset-0 bg-gradient-to-br from-emerald-600/30 to-teal-500/30 rounded-[3rem] blur-3xl opacity-20 group-hover:opacity-40 transition-all duration-700"
                        ></div>
                        <div
                            class="relative bg-gray-950/90 backdrop-blur-xl rounded-[2.5rem] shadow-[0_32px_64px_-16px_rgba(0,0,0,0.5)] overflow-hidden border border-white/10 transform transition-all duration-700 group-hover:scale-[1.02] group-hover:-rotate-1"
                        >
                            <div
                                class="flex items-center justify-between px-10 py-6 bg-white/5 border-b border-white/5"
                            >
                                <div class="flex space-x-2.5">
                                    <div
                                        class="w-3.5 h-3.5 rounded-full bg-rose-500/90 shadow-lg shadow-rose-500/20"
                                    ></div>
                                    <div
                                        class="w-3.5 h-3.5 rounded-full bg-amber-500/90 shadow-lg shadow-amber-500/20"
                                    ></div>
                                    <div
                                        class="w-3.5 h-3.5 rounded-full bg-emerald-500/90 shadow-lg shadow-emerald-500/20"
                                    ></div>
                                </div>
                                <div class="flex items-center space-x-2">
                                    <i
                                        class="ph ph-shield-check text-emerald-500/50 text-base"
                                    ></i>
                                    <span
                                        class="text-[10px] text-white/40 font-mono uppercase tracking-[0.3em]"
                                        >developer.yml</span
                                    >
                                </div>
                            </div>
                            <div class="p-12 font-mono text-sm leading-[1.8]">
                                <div class="text-emerald-400/90">
                                    <span
                                        class="text-emerald-500/60 font-black mr-4 text-xs opacity-30"
                                        >01</span
                                    >
                                    const
                                    <span class="text-teal-300">developer</span>
                                    = {
                                </div>
                                <div
                                    class="pl-5 mt-1 border-l border-emerald-500/10"
                                >
                                    <div class="text-white/80">
                                        <span
                                            class="text-emerald-500/60 font-black mr-4 text-xs opacity-30"
                                            >02</span
                                        >
                                        name:
                                        <span class="text-emerald-400"
                                            >"Abdullah Younas"</span
                                        >,
                                    </div>
                                    <div class="text-white/80">
                                        <span
                                            class="text-emerald-500/60 font-black mr-4 text-xs opacity-30"
                                            >03</span
                                        >
                                        role:
                                        <span class="text-emerald-400"
                                            >"Full Stack Architect"</span
                                        >,
                                    </div>
                                    <div class="text-white/80">
                                        <span
                                            class="text-emerald-500/60 font-black mr-4 text-xs opacity-30"
                                            >04</span
                                        >
                                        stack: [
                                    </div>
                                    <div class="pl-8 text-teal-400/90">
                                        <div
                                            class="flex items-center space-x-3"
                                        >
                                            <span
                                                class="text-emerald-500/60 font-black mr-1 text-xs opacity-30"
                                                >05</span
                                            >
                                            <span>"Laravel 12"</span>
                                        </div>
                                        <div
                                            class="flex items-center space-x-3"
                                        >
                                            <span
                                                class="text-emerald-500/60 font-black mr-1 text-xs opacity-30"
                                                >06</span
                                            >
                                            <span>"Vue 3"</span>
                                        </div>
                                        <div
                                            class="flex items-center space-x-3"
                                        >
                                            <span
                                                class="text-emerald-500/60 font-black mr-1 text-xs opacity-30"
                                                >07</span
                                            >
                                            <span>"Tailwind CSS 4"</span>
                                        </div>
                                    </div>
                                    <div class="text-white/80">
                                        <span
                                            class="text-emerald-500/60 font-black mr-4 text-xs opacity-30"
                                            >08</span
                                        >
                                        ],
                                    </div>
                                    <div class="text-white/80">
                                        <span
                                            class="text-emerald-500/60 font-black mr-4 text-xs opacity-30"
                                            >09</span
                                        >
                                        status:
                                        <span class="text-amber-400"
                                            >"available_now"</span
                                        >
                                    </div>
                                </div>
                                <div class="text-emerald-400/90 mt-1">
                                    <span
                                        class="text-emerald-500/60 font-black mr-4 text-xs opacity-30"
                                        >10</span
                                    >
                                    }
                                </div>
                            </div>
                            <div
                                class="absolute bottom-0 right-0 p-8 opacity-5"
                            >
                                <i
                                    class="ph-fill ph-code text-9xl text-white"
                                ></i>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>
