<script setup lang="ts">
import type { Experience } from '../types'

const experiences: Experience[] = [
  {
    role: 'Senior Full-Stack Developer & QA Engineer',
    company: 'Sentinel Tech',
    location: 'Bali, Indonesia',
    period: '2021 - Now',
  },
  {
    role: 'Software Developer',
    company: 'Credenxia',
    location: 'Perth, Australia',
    period: '2022 - 2023',
  },
  {
    role: 'Senior Quality Engineer',
    company: 'Bank Jago',
    location: 'Jakarta, Indonesia',
    period: '2021 - 2022',
  },
  {
    role: 'Senior Web Developer',
    company: 'Vi8e Interactive Pte Ltd',
    location: 'Singapore',
    period: '2014 - 2021',
  },
]
</script>

<template>
  <section id="experience" class="section">
    <h2 class="nes-text" style="font-size: 14px; margin-bottom: 1.5rem; text-align: center;">
      <i class="nes-icon coin is-small"></i>
      Where I've Been
    </h2>

    <div class="nes-container is-rounded">
      <div
        v-for="(exp, index) in experiences"
        :key="exp.company + exp.period"
        class="animate-slide-left"
        :class="`delay-${index + 1}`"
        style="padding: 1rem 0; border-bottom: 2px dashed #d4d4d4;"
      >
        <div style="display: flex; justify-content: space-between; align-items: flex-start; flex-wrap: wrap; gap: 0.5rem;">
          <div>
            <p class="nes-text is-primary" style="font-size: 10px; margin-bottom: 0.3rem;">
              {{ exp.role }}
            </p>
            <p style="font-size: 9px; opacity: 0.7;">
              {{ exp.company }} - {{ exp.location }}
            </p>
          </div>
          <span class="nes-badge">
            <span class="is-warning" style="width: 12em; text-align: center;">{{ exp.period }}</span>
          </span>
        </div>
      </div>
    </div>
  </section>
</template>
