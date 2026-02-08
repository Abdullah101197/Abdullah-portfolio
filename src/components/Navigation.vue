<script setup>
import { ref } from "vue";

defineProps({
    scrolled: Boolean,
});

const mobileMenuOpen = ref(false);

const navLinks = [
    { name: "Home", href: "#home" },
    { name: "Services", href: "#services" },
    { name: "Skills", href: "#skills" },
    { name: "Projects", href: "#projects" },
    { name: "Experience", href: "#experience" },
];
</script>

<template>
    <nav
        class="fixed w-full top-0 z-50 transition-all duration-300"
        :class="
            scrolled
                ? 'glass-effect shadow-lg border-b border-gray-100'
                : 'bg-transparent'
        "
    >
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-20">
                <a href="#home" class="flex items-center space-x-3 group">
                    <div class="relative">
                        <div
                            class="absolute inset-0 bg-gradient-to-r from-emerald-600 to-teal-600 rounded-xl blur opacity-75 group-hover:opacity-100 transition"
                        ></div>
                        <div
                            class="relative w-12 h-12 bg-gradient-to-br from-emerald-600 to-teal-600 rounded-xl flex items-center justify-center shadow-lg"
                        >
                            <span
                                class="text-white font-bold text-xl uppercase tracking-tighter"
                                >AY</span
                            >
                        </div>
                    </div>
                    <span
                        class="text-xl font-bold font-display hidden sm:block tracking-tight"
                        >Abdullah<span class="text-emerald-600">.</span></span
                    >
                </a>

                <div class="hidden md:flex items-center space-x-1">
                    <a
                        v-for="link in navLinks"
                        :key="link.name"
                        :href="link.href"
                        class="px-4 py-2 rounded-lg text-sm font-medium text-gray-700 hover:text-emerald-600 hover:bg-emerald-50 transition-all tracking-tight"
                    >
                        {{ link.name }}
                    </a>
                </div>

                <div class="hidden md:block">
                    <a
                        href="#contact"
                        class="relative inline-flex items-center px-6 py-3 rounded-full bg-gray-900 text-white font-semibold text-sm shadow-xl shadow-gray-200 hover:shadow-2xl transition-all duration-300 hover:scale-105 tracking-tight"
                    >
                        <span>Let's Talk</span>
                        <i class="ph-bold ph-arrow-right ml-2 text-xs"></i>
                    </a>
                </div>

                <button
                    @click="mobileMenuOpen = !mobileMenuOpen"
                    class="md:hidden p-2 rounded-lg text-gray-700 hover:bg-gray-100 active:scale-95 transition-transform"
                >
                    <i
                        class="ph text-2xl"
                        :class="mobileMenuOpen ? 'ph-x' : 'ph-list'"
                    ></i>
                </button>
            </div>
        </div>

        <!-- Mobile Menu -->
        <Transition
            enter-active-class="transition duration-300 ease-out"
            enter-from-class="opacity-0 -translate-y-4"
            enter-to-class="opacity-100 translate-y-0"
            leave-active-class="transition duration-200 ease-in"
            leave-from-class="opacity-100 translate-y-0"
            leave-to-class="opacity-0 -translate-y-4"
        >
            <div
                v-show="mobileMenuOpen"
                class="md:hidden glass-effect border-t border-gray-100"
            >
                <div class="px-4 py-6 space-y-2">
                    <a
                        v-for="link in navLinks"
                        :key="link.name"
                        :href="link.href"
                        @click="mobileMenuOpen = false"
                        class="block px-4 py-3 rounded-lg text-gray-700 hover:bg-emerald-50 hover:text-emerald-600 font-medium transition-colors"
                    >
                        {{ link.name }}
                    </a>
                    <a
                        href="#contact"
                        @click="mobileMenuOpen = false"
                        class="block px-4 py-4 mt-4 text-center rounded-xl bg-gray-900 text-white font-bold shadow-lg shadow-gray-200"
                    >
                        Let's Talk
                    </a>
                </div>
            </div>
        </Transition>
    </nav>
</template>
