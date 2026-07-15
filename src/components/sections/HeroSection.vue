<template>
  <div class="hero">
    <div class="hero-title-outer-box">
      <div class="hero-title-middle-box">
        <div class="box-top-left"></div>
        <div class="box-top-right"></div>
        <div class="box-bottom-left"></div>
        <div class="box-bottom-right"></div>
        <div class="hero-title-inner-box">
          <p class="hero-title">MRB<span class="hero-title-accent">LABS</span></p>
        </div>
      </div>
    </div>
    <div class="hero-accent" style="opacity: 0; transform: translateY(10px);">
      <div class="line" />
      <p>DEVELOPER</p>
      <div class="line line-reverse" />
    </div>
    <div class="hero-dev-name" style="opacity: 0; transform: translateY(10px);">
      <p>MrBobertus</p>
    </div>
    <div class="hero-notation-points" style="opacity: 0; transform: translateY(10px);">
      <Terminal :size="16" />
      <p>{{ mottoText }}</p><span class="hero-notation-point-cursor">_</span>
    </div>
    <div class="button-div" style="opacity: 0; transform: translateY(10px);">
      <button @click="emit('scroll-to-projects')" class="button1">PROJEKTE ANSEHEN</button>
      <button @click="emit('scroll-to-contact')" class="button2">KONTAKT AUFNEHMEN</button>
    </div>
    <div class="scroll-notice">
      <Mouse :size="22" />
    </div>
  </div>
</template>

<script setup>
  import { ref, onMounted } from 'vue'
  import { Terminal, Mouse } from 'lucide-vue-next'

  const emit = defineEmits(['scroll-to-projects','scroll-to-contact'])

  const mottoText = ref('')
  const fullText = "Entwicklung. Innovation. Präzision."
  const typingSpeed = 50

  onMounted(() => {
    let i = 0
    
    const typeWriter = () => {
      if (i < fullText.length) {
        mottoText.value += fullText.charAt(i)
        i++
        setTimeout(typeWriter, typingSpeed)
      }
    }

    setTimeout(() => {
      typeWriter()
    }, 1800)
  })
</script>

<style scoped>
.hero {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 100%;
  height: 100vh;
}

.hero-title-outer-box {
  background: none;
  border: 1px solid var(--border-hover);
  padding: 0.4rem;
  margin-top: 0.5rem;
  opacity: 0; transform: scale(0.9); animation: scaleInAnim 0.8s cubic-bezier(0.16, 1, 0.3, 1) forwards;
  transition: all 0.3s ease-in-out; 
}

.hero-title-middle-box {
  background: none;
  position: relative;
  padding: 0.4rem;
  transition: all 0.4s ease-in-out;
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
.box-top-right {
  position: absolute;
  top: 0;
  right: 0;
  height: 10px;
  width: 10px;
  border-top: 1px solid var(--accent);
  border-right: 1px solid var(--accent);
}
.box-bottom-left {
  position: absolute;
  bottom: 0;
  left: 0;
  height: 10px;
  width: 10px;
  border-bottom: 1px solid var(--accent);
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

.hero-title-inner-box {
  background-color: var(--bg-elevated);
  border: 1px solid var(--border-hover);
  padding: 1rem 2rem;
}

.hero-title {
  color: var(--text-primary);
  font-family: var(--font-main);
  font-size: 4.5rem;
  font-weight: 700;
  margin: 0;
  padding: 0;
}

.hero-accent {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  color: var(--accent);
  gap: 0.5rem;
  font-family: var(--font-mono);
  font-size: 0.65rem;
  margin-top: 1rem;
  animation: slideVertical 0.5s forwards;
  animation-delay: 0.8s;
}

.hero-dev-name {
  color: var(--text-secondary);
  margin: 0;
  padding: 0;
  font-weight: 300;
  font-size: 1.5rem;
  animation: slideVertical 0.5s forwards;
  animation-delay: 1.2s;
}

.hero-dev-name p {
  margin: 0;
  padding: 0;
}

.hero-title-accent {
  color: var(--bg-primary);
  text-shadow: -1px -1px 0 var(--accent-light), 1px -1px 0 var(--accent-light), -1px 1px 0 var(--accent-light), 1px 1px 0 var(--accent-light);
  margin-left: 1rem;
  transition: all 0.4s ease-in-out;
}

.hero-notation-points {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  font-family: var(--font-mono);
  color: var(--text-tertiary);
  font-size: 0.75rem;
  letter-spacing: 0.1rem;
  animation: slideVertical 0.5s forwards;
  animation-delay: 1.4s;
}

.hero-notation-points p {
    margin-left: 0.5rem;
}

.hero-notation-point-cursor {
  color: var(--accent);
  animation: blink 1s step-end infinite;
}

.button-div {
  margin-top: 2rem;
  animation: slideVertical 0.5s forwards;
  animation-delay: 1.8s;
}

.button1 {
  background: none;
  color: var(--text-primary);
  border: 1px solid var(--accent);
  font-family: var(--font-mono);
  font-size: 0.8rem;
  margin: 0;
  padding: 0.6rem 2rem;
  transition: all 0.2s ease;
}

.button1:hover {
  cursor: pointer;
  border: 1px solid var(--accent-light);
  background-color: var(--accent-light);
}

.button2 {
  background: none;
  font-family: var(--font-mono);
  color: var(--text-secondary);
  font-size: 0.8rem;
  border: none;
  margin: 0;
  padding: 0.6rem 2rem;
  transition: all 0.2s ease;
}

.button2:hover {
  cursor: pointer;
  color: var(--accent-light);
}

.scroll-notice {
  position: absolute;
  bottom: 2rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  color: var(--text-tertiary);
  font-family: var(--font-mono);
  font-size: 0.8rem;
  font-weight: 300;
  animation: hover 5s ease-in-out infinite;
}

.line {
  height: 1px;
  width: 2rem;
  background: linear-gradient(to right, transparent, rgba(139, 0, 0, 0.5));
}

.line-reverse {
  transform: scaleX(-1);
}

@media (max-width: 768px) {
  .hero {
    padding: 1.5rem;
    box-sizing: border-box;
    justify-content: center;
  }

  .hero-title {
    font-size: 2.5rem;
  }

  .hero-title-accent {
    margin-left: 0.5rem;
  }

  .hero-title-inner-box {
    padding: 0.8rem 1.5rem;
  }

  .hero-dev-name {
    font-size: 1.2rem;
  }

  .hero-notation-points {
    font-size: 0.65rem; 
    letter-spacing: 0.05rem;
    text-align: center;
    padding: 0 1rem;
  }

  .button-div {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 0.8rem;
    width: 100%;
    max-width: 280px;
    margin-top: 1.5rem;
  }

  .button1, .button2 {
    width: 100%;
    text-align: center;
    padding: 0.8rem 1rem; 
    box-sizing: border-box;
  }

  .button2 {
    border: 1px solid rgba(255, 255, 255, 0.1);
  }

  .scroll-notice {
    bottom: 1.5rem;
  }
}
</style>
