<script setup lang="ts">
import type { ContactLink } from '../types'

const links: ContactLink[] = [
  {
    label: 'herutrijaya13@gmail.com',
    url: 'mailto:herutrijaya13@gmail.com',
    icon: 'nes-icon gmail is-small',
  },
  {
    label: 'LinkedIn',
    url: 'https://linkedin.com/in/heru-trijaya-b1333511a',
    icon: 'nes-icon linkedin is-small',
  },
  {
    label: 'GitHub',
    url: 'https://github.com/elniteru',
    icon: 'nes-icon github is-small',
  },
]
</script>

<template>
  <section id="contact" class="section">
    <div class="nes-container is-rounded is-dark is-centered animate-step">
      <h2 class="nes-text" style="font-size: 16px; margin-bottom: 1rem;">
        Let's work together.
      </h2>
      <p style="font-size: 10px; margin-bottom: 2rem; opacity: 0.85;">
        I'm currently open to new opportunities. Drop me a message anytime.
      </p>

      <div style="display: flex; gap: 1rem; justify-content: center; flex-wrap: wrap;">
        <a
          v-for="link in links"
          :key="link.label"
          :href="link.url"
          target="_blank"
          rel="noopener"
          class="nes-btn"
        >
          <i :class="link.icon"></i>
          {{ link.label }}
        </a>
      </div>
    </div>
  </section>
</template>
