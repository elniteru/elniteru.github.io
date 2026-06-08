<script setup lang="ts">
import { ref, onMounted } from 'vue'

const titleText = 'I build software that actually ships.'
const displayText = ref('')
const showCursor = ref(true)
let charIndex = 0

onMounted(() => {
  const typeInterval = setInterval(() => {
    if (charIndex < titleText.length) {
      displayText.value += titleText[charIndex]
      charIndex++
    } else {
      clearInterval(typeInterval)
    }
  }, 60)

  setInterval(() => {
    showCursor.value = !showCursor.value
  }, 530)
})
</script>

<template>
  <section id="hero" class="section">
    <div class="nes-container is-rounded is-dark is-centered" style="animation: step-fade-in 0.8s steps(4) both;">
      <h1 class="hero-title" style="font-size: 18px; line-height: 2.2; margin-bottom: 1.5rem; min-height: 3.5em;">
        {{ displayText }}<span v-if="showCursor" class="cursor">_</span>
      </h1>
      <!-- Avatar -->
      <div style="margin-bottom: 2rem; animation: step-fade-in 0.8s steps(4) both; display: flex; justify-content: center;">
        <div class="nes-container is-rounded is-dark" style="padding: 8px;">
          <img 
            src="/avatar.png" 
            alt="Heru Trijaya"
            style="width: 120px; height: auto; image-rendering: pixelated;"
          />
        </div>
      </div>

      <p style="font-size: 10px; line-height: 2; margin-bottom: 2rem; opacity: 0.85;">
        Full-stack engineer with 11 years of experience turning complex problems into clean, scalable products - from hotel management systems to e-commerce platforms. Based in Bali - Open to Remote/Relocation.
      </p>

      <div style="display: flex; gap: 1rem; justify-content: center; flex-wrap: wrap;">
        <a href="mailto:herutrijaya13@gmail.com" class="nes-btn is-primary animate-bounce">Say hello</a>
        <a href="https://github.com/elniteru" target="_blank" rel="noopener" class="nes-btn">View GitHub</a>
      </div>
    </div>
  </section>
</template>

<style scoped>
.cursor {
  animation: blink-cursor 0.8s steps(1) infinite;
  color: #209cee;
}
</style>
