<script setup>
import { portfolioData } from "../data/mockData";
const { personalInfo } = portfolioData;
</script>

<template>
    <section
        id="contact"
        class="relative py-40 overflow-hidden bg-[#020617] bg-grain"
    >
        <!-- Sophisticated Dark Background Decor -->
        <div class="absolute inset-0 z-0">
            <div
                class="absolute top-[-10%] left-[-10%] w-[800px] h-[800px] bg-emerald-900/10 rounded-full blur-[160px] animate-float opacity-30"
            ></div>
            <div
                class="absolute bottom-[-10%] right-[-10%] w-[800px] h-[800px] bg-teal-900/10 rounded-full blur-[160px] opacity-30"
                style="animation: float 10s ease-in-out infinite reverse"
            ></div>
            <div
                class="absolute inset-0 bg-[radial-gradient(rgba(255,255,255,0.03)_1px,transparent_1px)] [background-size:40px_40px]"
            ></div>
        </div>

        <div
            class="relative z-10 max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 text-center"
        >
            <div
                class="inline-flex items-center space-x-2 px-3 py-1 rounded-full bg-emerald-500/10 border border-emerald-500/20 mb-10"
            >
                <span
                    class="text-[10px] font-black text-emerald-400 uppercase tracking-[0.2em]"
                    >Available for projects</span
                >
            </div>

            <h2
                class="text-6xl lg:text-[120px] font-black font-display text-white mb-10 tracking-tighter leading-[0.85]"
            >
                Let's Build <span class="text-gradient">Something Elite</span>
            </h2>

            <p
                class="text-xl text-gray-400 mb-20 max-w-2xl mx-auto font-medium tracking-tight leading-relaxed"
            >
                Currently taking on limited high-impact projects. Whether you're
                a startup or enterprise, let's engineer your success.
            </p>

            <div
                class="flex flex-col sm:flex-row gap-8 justify-center items-center mb-32"
            >
                <a
                    :href="personalInfo.whatsapp"
                    target="_blank"
                    class="group relative inline-flex items-center justify-center px-12 py-6 rounded-[2.5rem] bg-emerald-500 text-white font-black text-xl shadow-[0_32px_64px_-16px_rgba(16,185,129,0.3)] hover:shadow-[0_48px_80px_-16px_rgba(16,185,129,0.5)] transition-all duration-300 hover:scale-105 active:scale-95 overflow-hidden"
                >
                    <div
                        class="absolute inset-0 bg-white/10 opacity-0 group-hover:opacity-100 transition-opacity"
                    ></div>
                    <i
                        class="ph-fill ph-whatsapp-logo text-3xl mr-4 group-hover:rotate-12 transition-transform"
                    ></i>
                    <span class="tracking-tighter">WhatsApp Consultation</span>
                </a>

                <a
                    href="mailto:abdullahyounas@example.com"
                    class="group inline-flex items-center justify-center px-10 py-6 rounded-[2.5rem] bg-white/5 backdrop-blur-md text-white font-bold text-lg border border-white/10 hover:border-emerald-500/50 hover:bg-white/10 transition-all duration-300 hover:scale-105 active:scale-95"
                >
                    <i
                        class="ph-bold ph-envelope text-2xl mr-4 text-emerald-400 transition-transform group-hover:-rotate-12"
                    ></i>
                    <span class="tracking-tight">Direct Inquiry</span>
                </a>
            </div>

            <!-- Social Ecosystem -->
            <div class="pt-20 border-t border-white/5">
                <div
                    class="grid grid-cols-2 md:grid-cols-4 gap-8 lg:gap-12 max-w-4xl mx-auto"
                >
                    <div
                        v-for="social in [
                            { name: 'GitHub', icon: 'ph-bold ph-github-logo' },
                            {
                                name: 'LinkedIn',
                                icon: 'ph-bold ph-linkedin-logo',
                            },
                            {
                                name: 'Twitter',
                                icon: 'ph-bold ph-twitter-logo',
                            },
                            {
                                name: 'Instagram',
                                icon: 'ph-bold ph-instagram-logo',
                            },
                        ]"
                        :key="social.name"
                        class="group relative"
                    >
                        <div
                            class="bg-white/5 rounded-[2rem] p-8 border border-white/[0.03] group-hover:bg-white/10 group-hover:border-emerald-500/30 transition-all duration-500 text-center"
                        >
                            <div
                                class="w-14 h-14 rounded-2xl bg-emerald-500/10 flex items-center justify-center mb-4 mx-auto group-hover:scale-110 group-hover:rotate-6 transition-all duration-500 border border-emerald-500/20"
                            >
                                <i
                                    :class="[
                                        social.icon,
                                        'text-2xl text-emerald-400',
                                    ]"
                                ></i>
                            </div>
                            <span
                                class="text-[10px] font-black text-gray-500 uppercase tracking-[0.2em] group-hover:text-white transition-colors"
                            >
                                {{ social.name }}
                            </span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>
