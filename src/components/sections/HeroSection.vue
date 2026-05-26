<template>
  <div class="hero">
    <div>
      <div class="dot" />
      <p class="tertiary-text"> WILKOMMEN, NUTZER...</p>
    </div>
    <div>
      <div>
        <div>
          <p>MRB<span class="text-red">LABS</span></p>
        </div>
      </div>
    </div>
    <div class="text-red">
      <p>DEVELOPER</p>
    </div>
  <div><div class="line" /><p class="secondary-text">MrBobertus</p><div class="line line-reverse" /></div>
    <div>
      <p class="tertiary-text">Entwicklung. Innovation. Präzision.<span class="text-red">_</span></p>
    </div>
    <div>
      <button>PROJEKTE ANSEHEN</button>
      <button>KONTAKT AUFNEHMEN</button>
    </div>
    <div>
      SCROLL
      <ChevronDown :size="16" class="icon" />
    </div>
  </div>
</template>

<script setup>
  import { ChevronDown } from 'lucide-vue-next'
</script>

<style scoped>
.hero {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 100%;
  height: 100vh
}

.secondary-text {
  color: var(--text-secondary);
  font-family: var(--font-main);
  margin: 0;
  padding: 0;
}

.tertiary-text {
  color: var(--text-tertiary);
  font-size: 0.7rem;
  text-align: left;
  font-family: var(--font-main);
  margin: 0;
  padding: 0;
}

.text-red {
  color: var(--accent-light);
}

.icon {
  color: var(--text-primary);
}

.line {
  height: 1px;
  width: 2rem;
  background: linear-gradient(to right, transparent, rgba(139, 0, 0, 0.5));
}

.line-reverse {
  transform: scaleX(-1);
}

.dot {
  width: 6px;
  height: 6px;
  border-radius: 50%;
  background-color: var(--accent-light);
  animation: pulse 1.5s infinite;
}

@keyframes pulse {
  0%, 100% { opacity: 1; }
  50% { opacity: 0.3; }
}
</style>