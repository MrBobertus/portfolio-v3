<template>
  <div class="projects">
    <div class="projects-section-info">
      <div class="line"></div>
      <p>03 // PROJEKTE</p>
    </div>
    <p class="projects-title">Ausgewählte <span class="projects-title-keyword">Arbeiten</span>?</p>
    <p class="projects-explanation">Eine Auswahl meiner besten Projekte. Von Unternehmenslösungen bis hin zu innovativen Experimenten.</p>
    <div class="project-list">
      <div class="project-box">
        <div class="box-top-left"></div>
        <div class="box-bottom-right"></div>
        <div class="button-menu">
          <button id="source-code-button" class="button1"><FileCode :size="16" /></button>
          <button id="showcase-button" class="button1"><SquareArrowOutUpRight :size="16" /></button>
        </div>
        <p class="project-number">01</p>
        <p class="project-title">Dashboard</p>
        <p class="project-class">SAAS PLAFTFORM</p>
        <p class="project-description">Eine moderne Analytics-Dashboard-Plattform mit Echtzeit-Datenvisualisierung, anpassbaren Widgets und rollenbasiertem Zugriffsmanagement.</p>
        <div class="project-tech-list">
          <p>VUE.js</p>
          <p>Python</p>
          <p>Javascript</p>
        </div>
      </div>
      <div class="project-box">
        <div class="box-top-left"></div>
        <div class="box-bottom-right"></div>
        <div class="button-menu">
          <button id="source-code-button" class="button1"><FileCode :size="16" /></button>
          <button id="showcase-button" class="button1"><SquareArrowOutUpRight :size="16" /></button>
        </div>
        <p class="project-number">01</p>
        <p class="project-title">Dashboard</p>
        <p class="project-class">SAAS PLAFTFORM</p>
        <p class="project-description">Eine moderne Analytics-Dashboard-Plattform mit Echtzeit-Datenvisualisierung, anpassbaren Widgets und rollenbasiertem Zugriffsmanagement.</p>
        <div class="project-tech-list">
          <p>VUE.js</p>
          <p>Python</p>
          <p>Javascript</p>
        </div>
      </div>
      <div class="project-box">
        <div class="box-top-left"></div>
        <div class="box-bottom-right"></div>
        <div class="button-menu">
          <button id="source-code-button" class="button1"><FileCode :size="16" /></button>
          <button id="showcase-button" class="button1"><SquareArrowOutUpRight :size="16" /></button>
        </div>
        <p class="project-number">01</p>
        <p class="project-title">Dashboard</p>
        <p class="project-class">SAAS PLAFTFORM</p>
        <p class="project-description">Eine moderne Analytics-Dashboard-Plattform mit Echtzeit-Datenvisualisierung, anpassbaren Widgets und rollenbasiertem Zugriffsmanagement.</p>
        <div class="project-tech-list">
          <p>VUE.js</p>
          <p>Python</p>
          <p>Javascript</p>
        </div>
      </div>
      <div class="project-box">
        <div class="box-top-left"></div>
        <div class="box-bottom-right"></div>
        <div class="button-menu">
          <button id="source-code-button" class="button1"><FileCode :size="16" /></button>
          <button id="showcase-button" class="button1"><SquareArrowOutUpRight :size="16" /></button>
        </div>
        <p class="project-number">01</p>
        <p class="project-title">Dashboard</p>
        <p class="project-class">SAAS PLAFTFORM</p>
        <p class="project-description">Eine moderne Analytics-Dashboard-Plattform mit Echtzeit-Datenvisualisierung, anpassbaren Widgets und rollenbasiertem Zugriffsmanagement.</p>
        <div class="project-tech-list">
          <p>VUE.js</p>
          <p>Python</p>
          <p>Javascript</p>
        </div>
      </div>
    </div>
    <a href="https://github.com/MrBobertus?tab=repositories" class="button2">ALLE PROJEKTE<ExternalLink :size="16" /></a>
  </div>
</template>

<script setup>
  import { ArrowUpRight, SquareArrowOutUpRight, FileCode, ExternalLink } from 'lucide-vue-next'
</script>

<style scoped>
  .projects {
    display: flex;
    flex-direction: column;
    align-items: start;
    justify-content: center;
    padding: 4rem;
  }

  .projects-section-info {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    color: var(--accent);
    gap: 0.5rem;
    font-family: var(--font-mono);
    font-size: 0.7rem;
  }

  .projects-title {
    font-family: var(--font-main);
    font-weight: 700;
    font-size: 2rem;
    margin: 0;
  }

  .projects-title-keyword {
    color: var(--accent);
  }

  .projects-explanation {
    color: var(--text-secondary);
  }

  .project-list {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    align-items: center;
    justify-content: center;
    gap: 2rem;
  }

  .project-box {
    display: flex;
    position: relative;
    flex-direction: column;
    align-items: start;
    justify-content: center;
    flex: 1;
    background: var(--bg-secondary);
    border: 1px solid var(--border-hover);
    padding: 2rem;
    margin: 0;
    gap: 0.5rem;
    transition: all 0.2s ease;
  }

  .project-box:hover {
    border: 1px solid var(--accent);
  }

  .project-box:hover .button-menu {
    opacity: 1;
  }

  .project-number {
    font-family: var(--font-mono);
    color: var(--accent);
    font-size: 0.75rem;
    margin: 0;
    padding: 0;
  }

  .project-title {
    font-family: var(--font-main);
    color: var(--text-primary);
    font-size: 1.2rem;
    margin: 0;
    padding: 0;
  }

  .project-class {
    font-family: var(--font-main);
    color: var(--text-tertiary);
    font-size: 0.8rem;
    margin: 0;
    padding: 0;
  }

  .project-description {
    font-family: var(--font-main);
    color: var(--text-secondary);
    font-size: 1rem;
    margin: 0;
    padding: 0;
    margin-top: 1rem;
  }

  .project-tech-list {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 0.8rem;
    margin-top: 1rem;
  }

  .project-tech-list p {
    display: flex;
    flex-direction: column;
    align-items: start;
    justify-content: center;
    flex: 1;
    font-size: 0.7rem;
    background: var(--bg-primary);
    border: 1px solid var(--border);
    padding: 0.5rem 1rem;
    margin: 0;
  }

  .button-menu {
    opacity: 0;
    position: absolute;
    display: flex;
    flex-direction: row;
    gap: 0.6rem;
    top: 0;
    right: 0;
    margin: 1rem;
    transition: all 0.2s ease;
  }

  .button1 {
    display: flex;
    align-items: center;
    background: none;
    border: 1px solid var(--border);
    font-family: var(--font-mono);
    color: var(--text-tertiary);
    font-size: 0.8rem;
    margin: 0;
    padding: 0.6rem;
    transition: all 0.2s ease;
  }

  .button1:hover {
    cursor: pointer;
    color: var(--text-secondary);
    border: 1px solid var(--accent);
  }

  .button2 {
    display: flex;
    align-items: center;
    gap: 0.5rem;
    background: none;
    color: var(--text-primary);
    border: 1px solid var(--accent);
    font-family: var(--font-mono);
    font-size: 0.8rem;
    margin-top: 2rem;
    padding: 0.6rem 2rem;
    transition: all 0.2s ease;
    text-decoration: none;
  }

  .button2:hover {
    cursor: pointer;
    border: 1px solid var(--accent-light);
    background-color: var(--accent-light);
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