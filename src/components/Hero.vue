<script setup>
import { portfolioData } from "../data/mockData";
const { personalInfo } = portfolioData;
</script>

<template>
    <section
        id="home"
        class="relative min-h-screen flex items-center justify-center overflow-hidden bg-[#020617] bg-grain"
    >
        <!-- Ultra-Premium Dynamic Mesh Background -->
        <div class="absolute inset-0 z-0 overflow-hidden">
            <div
                class="absolute top-[-20%] right-[-10%] w-[1000px] h-[1000px] bg-emerald-600/20 rounded-full blur-[160px] animate-blob"
            ></div>
            <div
                class="absolute bottom-[-20%] left-[-10%] w-[1000px] h-[1000px] bg-teal-600/20 rounded-full blur-[160px] animate-blob animation-delay-2000"
            ></div>
            <div
                class="absolute top-[20%] left-[20%] w-[600px] h-[600px] bg-indigo-600/10 rounded-full blur-[140px] animate-blob animation-delay-4000"
            ></div>

            <!-- Architectural Grid -->
            <div
                class="absolute inset-0 bg-[radial-gradient(rgba(255,255,255,0.05)_1px,transparent_1px)] [background-size:40px_40px] [mask-image:radial-gradient(ellipse_60%_60%_at_50%_50%,#000_70%,transparent_100%)]"
            ></div>
        </div>

        <div
            class="relative z-10 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-32 w-full"
        >
            <div class="grid lg:grid-cols-2 gap-20 items-center">
                <div class="text-center lg:text-left">
                    <!-- Status Badge -->
                    <div
                        class="inline-flex items-center space-x-3 px-4 py-2 rounded-full bg-white/5 backdrop-blur-xl border border-white/10 mb-10 card-hover shadow-2xl"
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
                            class="text-[10px] font-black text-emerald-400 uppercase tracking-[0.3em]"
                            >System Online: Available</span
                        >
                    </div>

                    <!-- Architectural Headline -->
                    <h1
                        class="text-7xl sm:text-8xl lg:text-[130px] font-black font-display leading-[0.8] mb-12 tracking-tighter text-white"
                    >
                        <span class="relative inline-block">
                            ENGINEER
                            <span
                                class="absolute -bottom-2 left-0 w-full h-1 bg-gradient-to-r from-emerald-500 to-transparent"
                            ></span>
                        </span>
                        <br />
                        <span
                            class="text-transparent bg-clip-text bg-gradient-to-r from-emerald-400 to-teal-500 italic"
                            >ELITE</span
                        >
                        <br />
                        <span
                            class="relative inline-block text-white/20"
                            style="
                                -webkit-text-stroke: 1px
                                    rgba(255, 255, 255, 0.2);
                            "
                        >
                            SOLUTIONS
                        </span>
                    </h1>

                    <p
                        class="text-xl text-gray-400 mb-14 leading-relaxed max-w-2xl mx-auto lg:mx-0 font-medium tracking-tight"
                    >
                        {{ personalInfo.description }}
                    </p>

                    <!-- Primary CTA -->
                    <div
                        class="flex flex-col sm:flex-row gap-6 justify-center lg:justify-start mb-24"
                    >
                        <a
                            :href="personalInfo.whatsapp"
                            target="_blank"
                            class="group relative inline-flex items-center justify-center px-12 py-6 rounded-[2.5rem] bg-emerald-500 text-white font-black text-xl shadow-[0_32px_64px_-16px_rgba(16,185,129,0.4)] hover:shadow-[0_48px_80px_-16px_rgba(16,185,129,0.6)] transition-all duration-300 hover:scale-105 active:scale-95 overflow-hidden"
                        >
                            <div
                                class="absolute inset-0 bg-white/10 opacity-0 group-hover:opacity-100 transition-opacity"
                            ></div>
                            <i
                                class="ph-fill ph-whatsapp-logo text-3xl mr-4 group-hover:rotate-12 transition-transform"
                            ></i>
                            <span class="tracking-tighter"
                                >Initiate Consultation</span
                            >
                        </a>
                        <a
                            href="#projects"
                            class="group inline-flex items-center justify-center px-10 py-6 rounded-[2.5rem] bg-white/5 backdrop-blur-md text-white font-bold text-lg border border-white/10 hover:border-emerald-500/50 hover:bg-white/10 transition-all duration-300 hover:scale-105 active:scale-95"
                        >
                            <span class="tracking-tight"
                                >Inspect Portfolio</span
                            >
                            <i
                                class="ph-bold ph-arrow-right ml-4 group-hover:translate-x-2 transition-transform"
                            ></i>
                        </a>
                    </div>

                    <!-- Glassy Stats -->
                    <div
                        class="flex flex-wrap items-center justify-center lg:justify-start gap-8"
                    >
                        <div
                            v-for="stat in [
                                {
                                    label: 'Experience',
                                    value: personalInfo.experience,
                                    icon: 'ph-duotone ph-briefcase',
                                },
                                {
                                    label: 'Built Assets',
                                    value: '30+',
                                    icon: 'ph-duotone ph-cube',
                                },
                                {
                                    label: 'SLA Success',
                                    value: '100%',
                                    icon: 'ph-duotone ph-seal-check',
                                },
                            ]"
                            :key="stat.label"
                            class="group bg-white/5 backdrop-blur-xl border border-white/5 p-6 rounded-[2rem] hover:bg-white/10 transition-all duration-500 hover:border-emerald-500/30"
                        >
                            <div class="flex items-center space-x-4">
                                <div
                                    class="w-12 h-12 rounded-2xl bg-emerald-500/10 flex items-center justify-center group-hover:scale-110 transition-transform"
                                >
                                    <i
                                        :class="[
                                            stat.icon,
                                            'text-2xl text-emerald-400',
                                        ]"
                                    ></i>
                                </div>
                                <div>
                                    <div
                                        class="text-3xl font-black text-white tracking-tighter leading-none"
                                    >
                                        {{ stat.value }}
                                    </div>
                                    <div
                                        class="text-[10px] font-bold text-gray-500 uppercase tracking-widest mt-1"
                                    >
                                        {{ stat.label }}
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Elite 3D Code Environment -->
                <div class="relative hidden lg:block perspective-2000">
                    <div class="relative group animate-float translate-z-20">
                        <!-- Floating Decorative Asset -->
                        <div
                            class="absolute -top-12 -right-12 w-32 h-32 bg-emerald-500/20 rounded-full blur-2xl animate-pulse"
                        ></div>
                        <div
                            class="absolute -bottom-12 -left-12 w-32 h-32 bg-teal-500/20 rounded-full blur-2xl animate-pulse delay-700"
                        ></div>

                        <div
                            class="relative bg-[#020617] backdrop-blur-2xl rounded-[3rem] shadow-[0_60px_100px_-20px_rgba(0,0,0,0.8)] overflow-hidden border border-white/10 transform transition-all duration-1000 group-hover:rotate-x-6 group-hover:rotate-y-12"
                        >
                            <div
                                class="flex items-center justify-between px-10 py-7 bg-white/5 border-b border-white/5"
                            >
                                <div class="flex space-x-3">
                                    <div
                                        class="w-3.5 h-3.5 rounded-full bg-[#ff5f56]"
                                    ></div>
                                    <div
                                        class="w-3.5 h-3.5 rounded-full bg-[#ffbd2e]"
                                    ></div>
                                    <div
                                        class="w-3.5 h-3.5 rounded-full bg-[#27c93f]"
                                    ></div>
                                </div>
                                <div class="flex items-center space-x-3">
                                    <div
                                        class="px-3 py-1 rounded-lg bg-emerald-500/10 border border-emerald-500/20"
                                    >
                                        <span
                                            class="text-[9px] text-emerald-400 font-mono tracking-[0.2em] font-black uppercase"
                                            >Production Stage</span
                                        >
                                    </div>
                                </div>
                            </div>

                            <div class="p-14 font-mono text-base leading-[2]">
                                <div class="space-y-1">
                                    <div
                                        class="text-emerald-400/90 whitespace-nowrap"
                                    >
                                        <span class="text-pink-500">class</span>
                                        <span class="text-teal-300"
                                            >Architect</span
                                        >
                                        {
                                    </div>
                                    <div class="pl-8 border-l border-white/5">
                                        <div class="text-blue-400">
                                            constructor<span class="text-white"
                                                >() {</span
                                            >
                                        </div>
                                        <div class="pl-8 text-white/50">
                                            <div>
                                                this.<span class="text-teal-300"
                                                    >focus</span
                                                >
                                                =
                                                <span class="text-emerald-400"
                                                    >"Scalability"</span
                                                >;
                                            </div>
                                            <div>
                                                this.<span class="text-teal-300"
                                                    >credo</span
                                                >
                                                =
                                                <span class="text-emerald-400"
                                                    >"Performance First"</span
                                                >;
                                            </div>
                                        </div>
                                        <div class="text-white">}</div>

                                        <div class="mt-4 text-pink-500">
                                            async
                                            <span class="text-blue-400"
                                                >deploy</span
                                            ><span class="text-white"
                                                >(vision) {</span
                                            >
                                        </div>
                                        <div class="pl-8 text-white/50">
                                            <div
                                                class="flex items-center space-x-2"
                                            >
                                                <span class="text-pink-500"
                                                    >return await</span
                                                >
                                                <span class="text-indigo-400"
                                                    >transform</span
                                                >(vision);
                                            </div>
                                        </div>
                                        <div class="text-white">}</div>
                                    </div>
                                    <div class="text-emerald-400/90">}</div>
                                </div>
                            </div>

                            <!-- Decorative Watermark Icon -->
                            <div
                                class="absolute bottom-10 right-10 opacity-10 group-hover:opacity-20 transition-opacity"
                            >
                                <i
                                    class="ph-fill ph-sketch-logo text-8xl text-emerald-400"
                                ></i>
                            </div>
                        </div>

                        <!-- Extra depth layer: Floating Badge -->
                        <div
                            class="absolute -right-10 top-1/2 bg-white/10 backdrop-blur-2xl border border-white/20 p-4 rounded-2xl shadow-2xl transform hover:scale-110 transition-transform cursor-pointer"
                        >
                            <i
                                class="ph-fill ph-code text-3xl text-emerald-400"
                            ></i>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped>
@keyframes blob {
    0% {
        transform: translate(0px, 0px) scale(1);
    }
    33% {
        transform: translate(30px, -50px) scale(1.1);
    }
    66% {
        transform: translate(-20px, 20px) scale(0.9);
    }
    100% {
        transform: translate(0px, 0px) scale(1);
    }
}

.animate-blob {
    animation: blob 7s infinite;
}

.animation-delay-2000 {
    animation-delay: 2s;
}

.animation-delay-4000 {
    animation-delay: 4s;
}

.perspective-2000 {
    perspective: 2000px;
}

.rotate-x-6 {
    transform: rotateX(6deg);
}

.rotate-y-12 {
    transform: rotateY(12deg);
}

.translate-z-20 {
    transform: translateZ(20px);
}
</style>
