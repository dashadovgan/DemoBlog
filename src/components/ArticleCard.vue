<template>
  <router-link 
    :to="`/article/${id}`"
    class="bg-surface-container-lowest rounded-xl p-8 tactile-shadow-sm tactile-shadow-hover flex flex-col justify-between group cursor-pointer h-full"
    :class="[isLarge ? 'md:col-span-8' : 'md:col-span-4']"
  >
    <div class="space-y-4">
      <div class="flex justify-between items-start">
        <span class="bg-secondary-container/20 text-primary-container px-3 py-1 rounded-full font-label text-label-md inline-block">
          {{ category }}
        </span>
        <button class="text-outline hover:text-primary transition-colors" @click.stop.prevent="">
          <span class="material-symbols-outlined">bookmark_border</span>
        </button>
      </div>

      <div v-if="!isLarge && image" class="h-48 w-full overflow-hidden rounded-lg mb-4">
        <img :src="image" :alt="title" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500" />
      </div>

      <h2 
        class="text-on-surface group-hover:text-primary-container transition-colors"
        :class="[isLarge ? 'font-display text-headline-md-mobile md:text-headline-md' : 'font-display text-title-lg']"
      >
        {{ title }}
      </h2>
      
      <p class="font-body text-body-md text-on-surface-variant line-clamp-3">
        {{ excerpt }}
      </p>
    </div>

    <div class="mt-stack-md flex items-center justify-between border-t border-outline-variant/20 pt-4">
      <div class="flex items-center gap-3">
        <div v-if="authorImage" class="w-10 h-10 rounded-full bg-surface-variant overflow-hidden">
          <img :src="authorImage" :alt="authorName" class="w-full h-full object-cover" />
        </div>
        <span class="font-label text-label-md text-on-surface">{{ authorName || 'Dr. Sarah Jenkins' }}</span>
      </div>
      <span class="text-outline font-label text-label-md">{{ date }}</span>
    </div>
  </router-link>
</template>

<script setup lang="ts">
defineProps<{
  id: string | number
  title: string
  excerpt: string
  category: string
  date: string
  authorName?: string
  authorImage?: string
  image?: string
  isLarge?: boolean
}>()
</script>
