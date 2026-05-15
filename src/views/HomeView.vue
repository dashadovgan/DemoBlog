<script setup lang="ts">
import ArticleCard from '../components/ArticleCard.vue'

const featuredArticle = {
  id: 'bread-units',
  title: 'Understanding Bread Units: A Gentle Guide to Carbs',
  excerpt: 'Navigating meals doesn\'t have to feel like a math exam. Discover a softer, more intuitive approach to managing your daily intake while still enjoying the foods you love. We break down the essentials with empathetic clarity.',
  category: 'Education',
  readTime: '8 min read',
  image: 'https://lh3.googleusercontent.com/aida-public/AB6AXuAJJM5Ys1oJvtiXJb_novm3e-Iy9YIXl9ZHO-49iIHVOFSbAJn3UGFLIDAXjJDUNUEGQ0YoftE6xa1qRXP2Q4rNkEi5f-9uTa5bG3VMqzkQMqHe3uIfE2Vfjhj3HJfd82l-ifR56EVGWAZeglxeoWO2Ob-qHPw8Lb70GHhUHzx69TyoGJA3MM9Z5JhfE9eZ9Z4Bb8k79fVn4HrWk4OvZRswn16LM6fssAOK3Eyf40DYMrYirN3Vicr2evIxTBD80UDKoTXk4DpQN4wG'
}

const articles = [
  {
    id: 'finding-calm',
    isLarge: true,
    title: 'Finding Calm in the Daily Routine',
    excerpt: 'Managing diabetes often feels like a full-time job. We explore simple, grounding techniques to weave moments of peace into your schedule, reducing the emotional friction of daily checks and balances.',
    category: 'Mindfulness',
    date: 'Oct 12',
    authorName: 'Dr. Sarah Jenkins',
    authorImage: 'https://lh3.googleusercontent.com/aida-public/AB6AXuBuZMAdFSPcXBdFImeZRyV3NAh8nOdB_3aEvE41MLDXUEMoLPTESKoMXZ9MKoJT6wXWC1tOx5cau2bsyxrQJMdKdmm1o2sPZH6uTswo077vPxqGXm3JozxeV8i-oskp11IUW0foX8nETur9AxEyoo3MQr3MF3ce5DrPb8mGhV5VlbWvkjvfV8JTEt-rrdnsTsCN1KeVy9zGkDBDad--6XkMOmiVzCWks1j4GqKz0utlUqYIvtLtmdmmlPeIWQmwgjuP8ehoNhSbE2tc'
  },
  {
    id: 'morning-bowls',
    title: 'Low-Impact Morning Bowls',
    excerpt: 'Start your day with steady energy. These three bowl recipes are designed to be gentle on your blood sugar.',
    category: 'Recipes',
    date: 'Oct 10',
    image: 'https://lh3.googleusercontent.com/aida-public/AB6AXuDMmxkZ15djvnu2kw24XcluryAA559BsJtuGYPFCRSdhF5boLhS6FXfQ3J2i7BEtDV-eObKDTYDxz04RhNoPTRelfwF-CaWwWJiKxGMs1t6nv27PXDP07waNGLBEW3bsYdUstejAi8guwMb56hpw03tAcbrzf6DtY0eyGh9EUOhrWKWt2utLJex2vy7bjZ02y2RDCCPJbZmRiWnRX42UWlgvuIk8VdyEJUufkmc2Mcjg-nKYB4FhFb2-fFcYwZTekaBlX_OL4nGe3H3'
  }
]
</script>

<template>
  <div class="w-full max-w-container-max mx-auto px-margin-mobile md:px-gutter pt-stack-lg pb-section-padding space-y-section-padding">
    
    <!-- Hero Section -->
    <section class="grid grid-cols-1 md:grid-cols-12 gap-gutter items-center">
      <div class="md:col-span-7 space-y-stack-md order-2 md:order-1">
        <div class="inline-flex items-center gap-2 bg-secondary-container/20 text-primary-container px-3 py-1 rounded-full font-label text-label-md">
          <span class="material-symbols-outlined text-sm fill">star</span>
          Featured Article
        </div>
        <h1 class="font-display text-display-lg-mobile md:text-display-lg text-on-surface leading-tight">
          {{ featuredArticle.title }}
        </h1>
        <p class="font-body text-body-lg text-on-surface-variant max-w-2xl">
          {{ featuredArticle.excerpt }}
        </p>
        <div class="flex items-center gap-4 pt-4">
          <router-link 
            :to="`/article/${featuredArticle.id}`"
            class="bg-primary-container text-on-primary px-6 py-3 rounded-lg font-label text-label-md hover:bg-primary transition-colors duration-300 tactile-shadow-sm"
          >
            Read the Guide
          </router-link>
          <span class="text-on-surface-variant font-label text-label-md flex items-center gap-1">
            <span class="material-symbols-outlined text-sm">schedule</span> {{ featuredArticle.readTime }}
          </span>
        </div>
      </div>
      <div class="md:col-span-5 order-1 md:order-2">
        <div class="rounded-xl overflow-hidden tactile-shadow-md aspect-[4/3] md:aspect-[3/4] relative">
          <img :src="featuredArticle.image" alt="Featured Article Image" class="object-cover w-full h-full" />
        </div>
      </div>
    </section>

    <!-- Filters -->
    <section class="border-y border-outline-variant/30 py-6 flex overflow-x-auto no-scrollbar gap-4 items-center">
      <span class="text-on-surface-variant font-label text-label-md mr-2 whitespace-nowrap">Explore Topics:</span>
      <button class="bg-primary-container text-on-primary px-4 py-2 rounded-full font-label text-label-md shrink-0">All Posts</button>
      <button class="bg-secondary-container/20 text-primary-container hover:bg-secondary-container/40 px-4 py-2 rounded-full font-label text-label-md shrink-0">Recipes</button>
      <button class="bg-secondary-container/20 text-primary-container hover:bg-secondary-container/40 px-4 py-2 rounded-full font-label text-label-md shrink-0">Education</button>
      <button class="bg-secondary-container/20 text-primary-container hover:bg-secondary-container/40 px-4 py-2 rounded-full font-label text-label-md shrink-0">Mindfulness</button>
    </section>

    <!-- Article Feed -->
    <section class="grid grid-cols-1 md:grid-cols-12 gap-gutter">
      <div v-for="article in articles" :key="article.id" :class="[article.isLarge ? 'md:col-span-8' : 'md:col-span-4']">
        <ArticleCard v-bind="article" />
      </div>
    </section>

  </div>
</template>
