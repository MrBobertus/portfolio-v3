<template>
  <div class="contact">
    <div class="contact-section-info">
      <div class="line"></div>
      <p>04 // KONTAKT</p>
    </div>
    <p class="contact-title">Irgendwelche <span class="contact-title-keyword">Fragen</span>?</p>
    <p class="contact-explanation">Hast du eine Frage im Kopf oder benötigtst du hilfe? Schreib mir, vielleicht kann ich ja helfen.</p>
  </div>
</template>

<script setup>
  import { CodeXml } from 'lucide-vue-next'
</script>

<style scoped>
  .contact {
    display: flex;
    flex-direction: column;
    align-items: start;
    justify-content: center;
    padding: 4rem;
  }

  .contact-section-info {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    color: var(--accent);
    gap: 0.5rem;
    font-family: var(--font-mono);
    font-size: 0.7rem;
  }

  .contact-title {
    font-family: var(--font-main);
    font-weight: 700;
    font-size: 2rem;
    margin: 0;
  }

  .contact-title-keyword {
    color: var(--accent);
  }

  .contact-explanation {
    color: var(--text-secondary);
  }

  .box-top-left {
    position: absolute;
    top: 0;
    left: 0;
    height: 10px;
    width: 10px;
    border-top: 1px solid var(--accent);
    border-left: 1px solid var(--accent);
  }
  .box-bottom-right {
    position: absolute;
    bottom: 0;
    right: 0;  
    height: 10px;
    width: 10px;
    border-bottom: 1px solid var(--accent);
    border-right: 1px solid var(--accent);
  }

  .line {
    height: 3px;
    width: 3.2rem;
    background: linear-gradient(to right, transparent, rgba(139, 0, 0, 0.5));
  }
</style>