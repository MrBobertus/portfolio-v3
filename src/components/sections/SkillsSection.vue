<template>
  <div class="skills">
    <div class="skill-section-info">
      <div class="line"></div>
      <p>02 // SKILLS</p>
    </div>
    <p class="skill-title">Die <span class="skill-title-keyword">Technologien</span> mit den ich arbeite.</p>
    <p class="skill-explanation">Hier ist eine Auswahl der Technologien und Tools, mit denen ich Projekte entwickle und zum Leben erwecke.</p>
      <div class="skill-container">
        <p class="skill-section-title"><codeXml :size="16" class="skill-section-icon" />FRONTEND</p>
        <div class="skill-list">
          <div class="skill-box">
            <div class="box-top-left"></div>
            <div class="box-bottom-right"></div>
            <img class="logo" src="https://placehold.co/400" width="50" height="50" alt="Skill Icon"/>
            <p class="skill-name">HTML</p>
          </div>
          <div class="skill-box">
            <div class="box-top-left"></div>
            <div class="box-bottom-right"></div>
            <img class="logo" src="https://placehold.co/400" width="50" height="50" alt="Skill Icon"/>
            <p class="skill-name">VUE.js</p>
          </div>
          <div class="skill-box">
            <div class="box-top-left"></div>
            <div class="box-bottom-right"></div>
            <img class="logo" src="https://placehold.co/400" width="50" height="50" alt="Skill Icon"/>
            <p class="skill-name">Javascript</p>
          </div>
        </div>
        <p class="skill-section-title"><codeXml :size="16" class="skill-section-icon" />BACKEND</p>
        <div class="skill-list">
          <div class="skill-box">
            <div class="box-top-left"></div>
            <div class="box-bottom-right"></div>
            <img class="logo" src="https://placehold.co/400" width="50" height="50" alt="Skill Icon"/>
            <p class="skill-name">Java</p>
          </div>
          <div class="skill-box">
            <div class="box-top-left"></div>
            <div class="box-bottom-right"></div>
            <img class="logo" src="https://placehold.co/400" width="50" height="50" alt="Skill Icon"/>
            <p class="skill-name">Python</p>
          </div>
        </div>
        <p class="skill-section-title"><codeXml :size="16" class="skill-section-icon" />TOOLS & SONSTIGES</p>
        <div class="skill-list">
          <div class="skill-box">
            <div class="box-top-left"></div>
            <div class="box-bottom-right"></div>
            <img class="logo" src="https://placehold.co/400" width="50" height="50" alt="Skill Icon"/>
            <p class="skill-name">Photoshop</p>
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

  .skill-section-icon {
    margin-right: 0.5rem;
  }

  .skill-section-title {
    font-size: 1.4rem;
    text-align: center;
  }

  .skill-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: start;
    gap: 0.5rem;
    width: 100%;
  }

  .skill-list {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 0.8rem;
  }

  .skill-box {
    display: flex;
    position: relative;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    flex: 1;
    background: var(--bg-elevated);
    border: 1px solid var(--border-hover);
    padding: 0.3rem 1.2rem;
    margin: 0;
    gap: 1rem;
  }

  .skill-name {
    color: var(--text-primary);
    font-size: 1rem;
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

  .logo {
    padding: 0.3rem;
  }

  .line {
    height: 3px;
    width: 3.2rem;
    background: linear-gradient(to right, transparent, rgba(139, 0, 0, 0.5));
  }
</style>