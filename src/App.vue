<template>
  <div id="app" :class="{ 'dark': isDarkMode }">
    <Navbar />
    <main>
      <router-view v-slot="{ Component, route }">
        <transition :name="route.meta.transition || 'fade'" mode="out-in">
          <component :is="Component" :key="route.path" />
        </transition>
      </router-view>
    </main>
    <Footer />
    
    <!-- Theme Toggle Button -->
    <button
      @click="toggleTheme"
      class="fixed bottom-8 right-8 z-50 p-4 bg-gradient-to-r from-primary-600 to-secondary-600 
                 rounded-full shadow-lg hover:shadow-xl transform hover:scale-110 transition-all duration-300"
      :aria-label="isDarkMode ? 'Switch to light mode' : 'Switch to dark mode'"
    >
      <Sun v-if="isDarkMode" class="w-6 h-6 text-white" />
      <Moon v-else class="w-6 h-6 text-white" />
    </button>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue'
import { useThemeStore } from '@/stores/index'
import Navbar from '@/components/Navbar.vue'
import Footer from '@/components/Footer.vue'
import { Sun, Moon } from 'lucide-vue-next'

const themeStore = useThemeStore()
const isDarkMode = ref(false)

const toggleTheme = () => {
  isDarkMode.value = !isDarkMode.value
  themeStore.toggleTheme()
  document.documentElement.classList.toggle('dark', isDarkMode.value)
}

onMounted(() => {
  isDarkMode.value = themeStore.isDarkMode
  document.documentElement.classList.toggle('dark', isDarkMode.value)
})
</script>

<style>
/* Page transitions */
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}

.slide-up-enter-active,
.slide-up-leave-active {
  transition: all 0.5s ease;
}

.slide-up-enter-from {
  transform: translateY(100%);
  opacity: 0;
}

.slide-up-leave-to {
  transform: translateY(-100%);
  opacity: 0;
}
</style>
