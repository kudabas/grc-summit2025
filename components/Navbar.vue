<template>
    <nav :class="[
        'fixed top-0 left-0 w-full z-50 transition-colors duration-300',
        isScrolled ? 'bg-white shadow-md text-black' : 'bg-transparent text-white'
    ]">
        <div class="max-w-7xl mx-auto px-4 py-3 flex items-center justify-between">
            <!-- Logo -->
            <NuxtLink to="/" class="flex items-center gap-2">
                <img src="@/assets/image/logo-grc.png" alt="Logo" class="h-12 w-auto" />
            </NuxtLink>

            <!-- Hamburger Button -->
            <button class="md:hidden focus:outline-none transition-all duration-200" @click="toggleMenu">
                <Icon :name="isMenuOpen ? 'mdi:close' : 'mdi:menu'" class="w-6 h-6 transition-transform duration-200" />
            </button>

            <!-- Desktop Nav Links -->
            <ul class="hidden md:flex gap-6 font-medium">
                <li><NuxtLink to="/detail" class="hover:underline">Session</NuxtLink></li>
                <li><NuxtLink to="/lifetime-achievement" class="hover:underline">Lifetime Achievement</NuxtLink></li>
                <li><NuxtLink to="/speakers" class="hover:underline">Speaker</NuxtLink></li>
                <li><NuxtLink to="/detail" class="hover:underline">Sponsorship</NuxtLink></li>
                <li><NuxtLink to="/reach-us" class="hover:underline">Reach Us</NuxtLink></li>
            </ul>
        </div>
    </nav>

    <!-- Mobile Overlay & Slide Menu -->
    <Transition name="slide-right">
        <div v-if="isMenuOpen" class=" fixed inset-0 z-40 flex md:hidden">
            <!-- Overlay -->
            <div class="flex-1 bg-black bg-opacity-50" @click="closeMenu"></div>

            <!-- Slide-in Menu -->
            <div class="pt-[100px] w-64 bg-blue-300 text-black p-6">
                <ul class="flex flex-col gap-4 font-medium">
                    <li><a href="#home" class="hover:underline" @click="closeMenu">Home</a></li>
                    <li><a href="#about" class="hover:underline" @click="closeMenu">About</a></li>
                    <li><a href="#contact" class="hover:underline" @click="closeMenu">Contact</a></li>
                </ul>
            </div>
        </div>
    </Transition>
</template>


<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const isScrolled = ref(false)
const isMenuOpen = ref(false)

const handleScroll = () => {
    isScrolled.value = window.scrollY > 10
}
const toggleMenu = () => {
    isMenuOpen.value = !isMenuOpen.value
}
const closeMenu = () => {
    isMenuOpen.value = false
}

onMounted(() => {
    window.addEventListener('scroll', handleScroll)
})
onUnmounted(() => {
    window.removeEventListener('scroll', handleScroll)
})
</script>
<style scoped>
.slide-right-enter-active,
.slide-right-leave-active {
    transition: all 0.3s ease;
}

.slide-right-enter-from {
    opacity: 0;
    transform: translateX(100%);
}

.slide-right-enter-to {
    opacity: 1;
    transform: translateX(0);
}

.slide-right-leave-from {
    opacity: 1;
    transform: translateX(0);
}

.slide-right-leave-to {
    opacity: 0;
    transform: translateX(100%);
}
</style>