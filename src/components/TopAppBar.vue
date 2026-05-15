<template>
  <header class="bg-surface shadow-sm sticky top-0 z-50 transition-shadow duration-300">
    <div class="flex justify-between items-center w-full px-margin-mobile md:px-gutter max-w-container-max mx-auto h-20">
      <button 
        aria-label="Menu" 
        class="text-primary hover:text-primary-fixed transition-colors duration-300 md:hidden p-2 -ml-2"
      >
        <span class="material-symbols-outlined text-[28px]">menu</span>
      </button>

      <router-link to="/" class="flex items-center">
        <div class="font-display text-headline-md-mobile md:text-headline-md text-primary italic font-bold">
          Diabetes Journal
        </div>
      </router-link>

      <!-- Desktop Nav -->
      <nav class="hidden md:flex gap-8 items-center">
        <router-link to="/" class="text-primary font-bold font-label text-label-md">Home</router-link>
        <a href="#" class="text-on-surface-variant hover:text-primary transition-colors font-label text-label-md">Library</a>
        <a href="#" class="text-on-surface-variant hover:text-primary transition-colors font-label text-label-md">Saved</a>
        <a href="#" class="text-on-surface-variant hover:text-primary transition-colors font-label text-label-md">Settings</a>
      </nav>

      <button 
        aria-label="Search" 
        class="text-primary hover:text-primary-fixed transition-colors duration-300 p-2 -mr-2"
      >
        <span class="material-symbols-outlined text-[28px]">search</span>
      </button>
    </div>
  </header>
</template>
