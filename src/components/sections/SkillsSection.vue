<template>
  <div class="skills">
    <div class="skill-section-info">
      <div class="line"></div>
      <p>02 // SKILLS</p>
    </div>
    <p class="skill-title">Die <span class="skill-title-keyword">Technologien</span> mit den ich arbeite.</p>
    <p class="skill-explanation">Hier ist eine Auswahl der Technologien und Tools, mit denen ich Projekte entwickle und zum Leben erwecke.</p>
      <div class="skill-container-list">
        <div class="skill-container">
          <div class="skill-container-header">
            <div class="skill-container-icon"><CodeXml :size="16" /></div>
            <div class="skill-container-header-text">
              <p class="skill-container-title">FRONTEND</p>
              <p class="skill-container-info">Moderne, performante Interfaces</p>
            </div>
          </div>
          <div class="skill-list">
            <p class="skill-name"><CodeXml :size="16" class="skill-icon" />Tailwind CSS</p>
            <p class="skill-name"><CodeXml :size="16" class="skill-icon" />Vue.js</p>
            <p class="skill-name"><CodeXml :size="16" class="skill-icon" />HTML / CSS / JS</p>
          </div>
        </div>
        <div class="skill-container">
          <div class="skill-container-header">
            <div class="skill-container-icon"><CodeXml :size="16" /></div>
            <div class="skill-container-header-text">
              <p class="skill-container-title">BACKEND</p>
              <p class="skill-container-info">Robuste API's & Datenbanken</p>
            </div>
          </div>
          <div class="skill-list">
            <p class="skill-name"><CodeXml :size="16" class="skill-icon" />Node.js</p>
            <p class="skill-name"><CodeXml :size="16" class="skill-icon" />Python</p>
            <p class="skill-name"><CodeXml :size="16" class="skill-icon" />Lua</p>
            <p class="skill-name"><CodeXml :size="16" class="skill-icon" />Java</p>
          </div>
        </div>
        <div class="skill-container">
          <div class="skill-container-header">
            <div class="skill-container-icon"><CodeXml :size="16" /></div>
            <div class="skill-container-header-text">
              <p class="skill-container-title">TOOLS & DEVOPS</p>
              <p class="skill-container-info">Workflows & Infrastruktur</p>
            </div>
          </div>
          <div class="skill-list">
            <p class="skill-name"><CodeXml :size="16" class="skill-icon" />Git / Github</p>
          </div>
        </div>
        <div class="skill-container">
          <div class="skill-container-header">
            <div class="skill-container-icon"><CodeXml :size="16" /></div>
            <div class="skill-container-header-text">
              <p class="skill-container-title">DESIGN</p>
              <p class="skill-container-info">UI/UX & Visuelle Systeme</p>
            </div>
          </div>
          <div class="skill-list">
            <p class="skill-name"><CodeXml :size="16" class="skill-icon" />Adobe Suite</p>
          </div>
        </div>
      </div>
  </div>
</template>

<script setup>
  import { CodeXml } from 'lucide-vue-next'
</script>

<style scoped>
  .skills {
    display: flex;
    flex-direction: column;
    align-items: start;
    justify-content: center;
    padding: 4rem;
  }

  .skill-section-info {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    color: var(--accent);
    gap: 0.5rem;
    font-family: var(--font-mono);
    font-size: 0.7rem;
  }

  .skill-title {
    font-family: var(--font-main);
    font-weight: 700;
    font-size: 2rem;
    margin: 0;
  }

  .skill-title-keyword {
    color: var(--accent);
  }

  .skill-explanation {
    color: var(--text-secondary);
  }

  .skill-container-list {
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: 1fr 1fr;
    gap: 1.5rem;
    width: 100%;
  }

  .skill-container {
    display: flex;
    position: relative;
    flex-direction: column;
    align-items: start;
    justify-content: start;
    flex: 1;
    background: var(--bg-elevated);
    border: 1px solid var(--border);
    padding: 2.2rem;
    margin: 0;
    gap: 1rem;
  }

  .skill-container-header {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    gap: 0.8rem;
  }

  .skill-container-header-text {
    display: flex;
    flex-direction: column;
    align-items: start;
    justify-content: center;
  }

  .skill-container-icon {
    display: flex;
    align-items: center;
    justify-content: center;
    color: var(--accent);
    border: 1px solid var(--accent);
    padding: 0.5rem;
  }

  .skill-container-title {
    font-size: 1.2rem;
    text-align: center;
    margin: 0;
  }

  .skill-container-info {
    color: var(--text-tertiary);
    font-size: 0.65rem;
    margin: 0;
    text-align: left;
  }

  .skill-name {
    display: flex;
    align-items: center;
    justify-content: center;
    border: 1px solid var(--border-hover);
    background: var(--bg-primary);
    color: var(--text-secondary);
    font-size: 0.7rem;
    text-align: center;
    padding: 0.5rem;
    margin: 0;
  }

  .skill-icon {
    color: var(--text-tertiary);
    margin-right: 0.5rem;
  }

  .skill-list {
    display: flex;
    flex-direction: row;
    gap: 0.8rem;
    flex-wrap: wrap;
    margin-top: 0.5rem;
  }

  .line {
    height: 3px;
    width: 3.2rem;
    background: linear-gradient(to right, transparent, rgba(139, 0, 0, 0.5));
  }
</style>