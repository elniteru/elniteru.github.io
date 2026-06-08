<script setup lang="ts">
const sections = [
  { id: 'about', label: 'About' },
  { id: 'skills', label: 'Skills' },
  { id: 'experience', label: 'Experience' },
  { id: 'contact', label: 'Contact' },
]

const scrollToSection = (id: string) => {
  const el = document.getElementById(id)
  if (el) {
    el.scrollIntoView({ behavior: 'smooth' })
  }
}
</script>

<template>
  <nav class="nes-container with-title is-centered">
    <p class="title" style="background-color: transparent; padding-top: 0.5rem;">Heru Trijaya</p>
    <div class="nav-links">
      <a
        v-for="section in sections"
        :key="section.id"
        class="nes-btn is-small"
        @click.prevent="scrollToSection(section.id)"
      >
        {{ section.label }}
      </a>
    </div>
  </nav>
</template>

<style scoped>
nav {
  margin-top: 2rem;
  margin-bottom: 2rem;
}

.nav-links {
  display: flex;
  gap: 0.5rem;
  justify-content: center;
  flex-wrap: wrap;
}

.nav-links .nes-btn {
  cursor: pointer;
}

nav > .title {
  flex-shrink: 0;
}
</style>
