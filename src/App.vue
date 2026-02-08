<script setup>
import { ref, onMounted } from "vue";
import Navigation from "./components/Navigation.vue";
import Hero from "./components/Hero.vue";
import Services from "./components/Services.vue";
import Skills from "./components/Skills.vue";
import Projects from "./components/Projects.vue";
import Experience from "./components/Experience.vue";
import Contact from "./components/Contact.vue";

const scrolled = ref(false);

onMounted(() => {
    window.addEventListener("scroll", () => {
        scrolled.value = window.pageYOffset > 50;
    });
});
</script>

<template>
    <div class="min-h-screen bg-white">
        <Navigation :scrolled="scrolled" />
        <main>
            <Hero />
            <Services />
            <Skills />
            <Projects />
            <Experience />
            <Contact />
        </main>
        <footer class="py-12 bg-gray-50 border-t border-gray-100">
            <div class="max-w-7xl mx-auto px-4 text-center">
                <p class="text-gray-500 font-medium tracking-tight">
                    &copy; {{ new Date().getFullYear() }} Abdullah Younas. All
                    rights reserved.
                </p>
            </div>
        </footer>
    </div>
</template>

<style>
/* App-wide styles if needed */
</style>
