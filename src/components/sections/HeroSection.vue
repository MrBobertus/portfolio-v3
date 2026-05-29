<template>
  <div class="hero">
    <div class="hero-welcome-message">
      <div class="dot" />
      <p>WILLKOMMEN, NUTZER.</p>
    </div>
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
    <div class="hero-accent">
      <div class="line" />
      <p>DEVELOPER</p>
      <div class="line line-reverse" />
    </div>
  <div class="hero-dev-name"><p>MrBobertus</p></div>
    <div class="hero-notation-points">
      <Terminal :size="16" />
      <p>Entwicklung. Innovation. Präzision.<span class="hero-notation-point-cursor">_</span></p>
    </div>
    <div class="button-div">
      <button class="button1">PROJEKTE ANSEHEN</button>
      <button class="button2">KONTAKT AUFNEHMEN</button>
    </div>
    <div class="scroll-notice">
      SCROLL
      <ChevronDown :size="16" />
    </div>
  </div>
</template>

<script setup>
  import { Terminal, ChevronDown } from 'lucide-vue-next'
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

.hero-welcome-message {
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 0.5rem;
  color: var(--text-tertiary);
  font-size: 0.6rem;
  text-align: left;
  font-family: var(--font-main);
  margin: 0;
  padding: 0;
}

.hero-title-outer-box {
  background: none;
  border: 1px solid var(--border-hover);
  padding: 0.4rem;
  margin-top: 0.5rem;
}

.hero-title-middle-box {
  background: none;
  position: relative;
  padding: 0.4rem;
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
}

.hero-dev-name {
  color: var(--text-secondary);
  margin: 0;
  padding: 0;
  font-weight: 300;
  font-size: 1.5rem;
}

.hero-dev-name p {
  margin: 0;
  padding: 0;
}

.hero-title-accent {
  color: var(--bg-primary);
  text-shadow: -1px -1px 0 var(--accent-light), 1px -1px 0 var(--accent-light), -1px 1px 0 var(--accent-light), 1px 1px 0 var(--accent-light);
  margin-left: 1rem;
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
}

.hero-notation-points p {
    margin-left: 0.5rem;
}

.hero-notation-point-cursor {
  color: var(--accent);
}

.button-div {
  margin-top: 2rem;
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
  bottom: 1rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  color: var(--text-tertiary);
  font-family: var(--font-mono);
  font-size: 0.8rem;
  font-weight: 300;
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