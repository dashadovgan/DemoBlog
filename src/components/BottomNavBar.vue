<template>
  <nav class="bg-surface-container-low shadow-md rounded-t-xl fixed bottom-0 left-0 w-full z-50 flex justify-around items-center py-3 px-4 transition-all">
    <router-link 
      to="/" 
      class="flex flex-col items-center justify-center transition-all p-2 rounded-lg"
      :class="[$route.name === 'home' ? 'bg-secondary-container text-on-secondary-container' : 'text-on-surface-variant']"
    >
      <span class="material-symbols-outlined text-[24px] mb-1" :class="{ 'fill': $route.name === 'home' }">home</span>
      <span class="font-label text-[10px]">Home</span>
    </router-link>
    
    <a class="flex flex-col items-center justify-center text-on-surface-variant p-2 rounded-lg" href="#">
      <span class="material-symbols-outlined text-[24px] mb-1">menu_book</span>
      <span class="font-label text-[10px]">Library</span>
    </a>
    
    <a class="flex flex-col items-center justify-center text-on-surface-variant p-2 rounded-lg" href="#">
      <span class="material-symbols-outlined text-[24px] mb-1">bookmark</span>
      <span class="font-label text-[10px]">Saved</span>
    </a>
    
    <a class="flex flex-col items-center justify-center text-on-surface-variant p-2 rounded-lg" href="#">
      <span class="material-symbols-outlined text-[24px] mb-1">settings</span>
      <span class="font-label text-[10px]">Settings</span>
    </a>
  </nav>
</template>

<script setup lang="ts">
import { useRoute } from 'vue-router';
const $route = useRoute();
</script>
