<script setup lang="ts">
import { RouterView } from 'vue-router'
import TopAppBar from './components/TopAppBar.vue'
import BottomNavBar from './components/BottomNavBar.vue'
import Footer from './components/Footer.vue'
</script>

<template>
  <div class="min-h-screen flex flex-col bg-surface text-on-surface">
    <TopAppBar />
    
    <main class="flex-grow">
      <RouterView v-slot="{ Component }">
        <transition 
          name="fade" 
          mode="out-in"
        >
          <component :is="Component" />
        </transition>
      </RouterView>
    </main>

    <Footer class="hidden md:flex" />
    <BottomNavBar class="md:hidden" />
  </div>
</template>

<style>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.3s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}

/* Material Symbols configuration */
.material-symbols-outlined {
  font-variation-settings: 'FILL' 0, 'wght' 400, 'GRAD' 0, 'opsz' 24;
  vertical-align: middle;
}
.material-symbols-outlined.fill {
  font-variation-settings: 'FILL' 1;
}
</style>
