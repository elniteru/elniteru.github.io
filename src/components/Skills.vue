<script setup lang="ts">
import type { Skill } from '../types'

const skills: Skill[] = [
  {
    title: 'Full-Stack Development',
    description: 'Go, PHP, TypeScript, Vue.js - building robust backends and polished frontends end to end.',
    icon: 'nes-icon heart is-small',
  },
  {
    title: 'QA Automation',
    description: 'Test suites with Cypress, Selenium, and Flutter Driver - integrated into CI/CD from day one.',
    icon: 'nes-icon like is-small',
  },
  {
    title: 'Cloud & DevOps',
    description: 'AWS-native architecture with CloudFormation, Lambda, and zero-downtime release pipelines.',
    icon: 'nes-icon star is-small',
  },
]
</script>

<template>
  <section id="skills" class="section">
    <h2 class="nes-text" style="font-size: 14px; margin-bottom: 1.5rem; text-align: center;">
      <i class="nes-icon star is-small"></i>
      What I Do
    </h2>

    <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 1.5rem;">
      <div
        v-for="(skill, index) in skills"
        :key="skill.title"
        class="nes-container is-rounded with-title animate-step"
        :class="`delay-${index + 1}`"
      >
        <p class="title" style="background-color: transparent; padding-top: 0.5rem;">{{ skill.title }}</p>
        <div style="text-align: center; margin-bottom: 0.75rem;">
          <i :class="skill.icon" style="font-size: 24px;"></i>
        </div>
        <p style="font-size: 9px; line-height: 2; text-align: center;">
          {{ skill.description }}
        </p>
      </div>
    </div>
  </section>
</template>
