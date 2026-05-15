<script setup lang="ts">
import { useRoute } from 'vue-router'

const route = useRoute()
// In a real app, we would fetch data based on route.params.id
</script>

<template>
  <article class="w-full max-w-3xl mx-auto px-margin-mobile md:px-gutter py-section-padding">
    <header class="mb-stack-lg text-center md:text-left">
      <div class="flex items-center justify-center md:justify-start gap-3 mb-stack-sm">
        <span class="font-label text-label-md bg-secondary-container/20 text-primary px-3 py-1 rounded-full uppercase tracking-wider">Nutrition</span>
        <span class="text-on-surface-variant text-sm flex items-center gap-1">
          <span class="material-symbols-outlined text-[16px]">schedule</span>
          5 min read
        </span>
      </div>
      <h1 class="font-display text-display-lg-mobile md:text-display-lg text-on-surface mb-stack-md leading-tight">
        Simple Guide to Low-Carb Breakfasts
      </h1>
      <p class="font-body text-body-lg text-on-surface-variant italic">
        Starting your day feeling grounded and steady. Discover gentle, nourishing ways to fuel your morning without the blood sugar spikes.
      </p>
    </header>

    <!-- Hero Image -->
    <div class="w-full aspect-[16/9] bg-surface-container-highest rounded-xl overflow-hidden mb-stack-lg shadow-sm">
      <img 
        src="https://lh3.googleusercontent.com/aida-public/AB6AXuBU8M0DRE-SkiKOW_Zc20-8bgoJkvj3QMWo_iytKOlXPt_cWLLFlzJjOfCgakt472jWcPMyT4vnOkftPw4JChBGl1eakgBHaPQekEKd8_khIWcrSrSiVI-8-tJVvLPspszsd4aR1s3PkS-vBtl_h58q-23UGgbPrG31ML6NXajdo_wVBXtC-XTIDU8GpDyjHrZWt0iKTU-FQ57MeG1KPGM-NHJo4Ce-ZGYlbGoce_w7FyUZeDXasJefetOgy8l5XR5lSqCNVMfePkII" 
        alt="Nourishing breakfast bowl" 
        class="w-full h-full object-cover" 
      />
    </div>

    <!-- Article Content -->
    <div class="prose max-w-none font-body text-body-lg text-on-surface leading-relaxed space-y-stack-md">
      <p>
        Mornings can often feel rushed, leaving little time to consider how our first meal impacts the rest of the day. For those of us managing our blood sugar, breakfast is a foundational moment—a chance to set a steady tone. Embracing a low-carb morning doesn't mean sacrificing comfort or flavor.
      </p>

      <div class="my-stack-lg bg-surface-container-low border-l-4 border-primary-container p-stack-md rounded-r-lg tactile-shadow-sm">
        <div class="flex items-start gap-3">
          <span class="material-symbols-outlined text-primary-container mt-1">lightbulb</span>
          <div>
            <h3 class="font-display text-title-lg text-on-surface mb-2">Gentle Reminder</h3>
            <p class="font-body text-body-md text-on-surface-variant m-0">
              Everyone's body responds differently. While these suggestions aim for steady blood sugar, always listen to your own body and consult with your care team.
            </p>
          </div>
        </div>
      </div>

      <h2 class="font-display text-title-lg text-on-surface mt-stack-lg mb-stack-sm border-b border-surface-variant pb-2">
        The Power of Protein
      </h2>
      <p>
        Protein is the cornerstone of a steady morning. It helps to slow digestion, keeping you feeling fuller for longer and blunting the impact of any carbohydrates you do consume.
      </p>

      <ul class="list-none space-y-4 pl-2 my-stack-md">
        <li class="flex items-start">
          <span class="text-primary-container mr-3 mt-1 text-[12px]">●</span>
          <span><strong>Eggs, Any Way:</strong> Scrambled, poached, or baked into a frittata. Eggs provide excellent, accessible protein.</span>
        </li>
        <li class="flex items-start">
          <span class="text-primary-container mr-3 mt-1 text-[12px]">●</span>
          <span><strong>Greek Yogurt:</strong> Opt for plain, full-fat Greek yogurt. It contains significantly more protein than regular yogurt.</span>
        </li>
      </ul>

      <h2 class="font-display text-title-lg text-on-surface mt-stack-lg mb-stack-sm border-b border-surface-variant pb-2">
        Embracing Healthy Fats
      </h2>
      
      <div class="grid grid-cols-1 md:grid-cols-2 gap-stack-md my-stack-lg">
        <div class="bg-surface-container-lowest p-stack-md rounded-xl shadow-sm border border-surface-variant">
          <span class="material-symbols-outlined text-secondary text-3xl mb-3">energy_savings_leaf</span>
          <h4 class="font-label text-label-md text-on-surface mb-2 uppercase tracking-wider">Avocado</h4>
          <p class="font-body text-body-md text-on-surface-variant text-sm">Rich in monounsaturated fats. Mash it with lime and sea salt.</p>
        </div>
        <div class="bg-surface-container-lowest p-stack-md rounded-xl shadow-sm border border-surface-variant">
          <span class="material-symbols-outlined text-secondary text-3xl mb-3">grain</span>
          <h4 class="font-label text-label-md text-on-surface mb-2 uppercase tracking-wider">Chia Seeds</h4>
          <p class="font-body text-body-md text-on-surface-variant text-sm">High in fiber and fat. Soak them overnight in almond milk.</p>
        </div>
      </div>

      <p>
        Building a new habit takes time and patience. Start by experimenting with one new recipe this week. Notice how you feel—the clarity of your mind, the steadiness of your energy. This journey is about finding what nourishes you, body and soul.
      </p>
    </div>
  </article>
</template>
