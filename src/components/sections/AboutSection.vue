<template>
  <div class="aboutme">
    <div class="aboutme-section1">
      <div class="aboutme-section-info">
        <div class="line"></div>
        <p>01 // ÜBER MICH</p>
      </div>
      <p class="aboutme-question">Wer steckt hinter <span class="aboutme-studio-name">MRB Labs</span>?</p>
      <div class="aboutme-question-answer">
        <p>
              Ich bin <span class="aboutme-developer-name">MrBobertus</span>, ein leidenschaftlicher
              Softwareentwickler mit Fokus auf moderne Webtechnologien. MRB Labs ist mein
              persönliches Studio für digitale Lösungen — ein Ort wo Technologie auf Design trifft.
            </p>
            <p>
              Meine Stärke liegt in der Kombination aus technischer Exzellenz und ästhetischem
              Feingefühl. Jedes Projekt wird mit derselben Präzision und Leidenschaft angegangen,
              egal ob es sich um eine komplexe Unternehmensanwendung oder ein minimalistisches
              Portfolio handelt.
            </p>
            <p>
              Ich glaube an sauberen Code, durchdachte Architektur und Designs die nicht nur
              gut aussehen, sondern auch intuitiv funktionieren.
            </p>
      </div>
      <div class="aboutme-stats">
        <div class="aboutme-stats-field">
          <div class="box-top-left"></div>
          <div class="box-bottom-right"></div>
          <p class="stat-value">2+</p>
          <p class="stat-text">JAHRE ERFAHRUNG</p>
        </div>
        <div class="aboutme-stats-field">
          <div class="box-top-left"></div>
          <div class="box-bottom-right"></div>
          <p class="stat-value">4+</p>
          <p class="stat-text">PROJEKTE</p>
        </div>
        <div class="aboutme-stats-field">
          <div class="box-top-left"></div>
          <div class="box-bottom-right"></div>
          <p class="stat-value">7+</p>
          <p class="stat-text">TECHNOLOGIEN</p>
        </div>
        <div class="aboutme-stats-field">
          <div class="box-top-left"></div>
          <div class="box-bottom-right"></div>
          <p class="stat-value">2+</p>
          <p class="stat-text">KUNDEN</p>
        </div>
      </div>
    </div>
    <div class="aboutme-section2">
      <div class="aboutme-keypoints">
        <div class="keypoint">
          <Terminal :size="16" class="keypoint-icon" />
          <p class="keypoint-title">Clean Code</p>
          <p class="keypoint-info">Strukturierter, wartbarer Code der Standards folgt.</p>
        </div>
        <div class="keypoint">
          <Terminal :size="16" class="keypoint-icon" />
          <p class="keypoint-title">Clean Code</p>
          <p class="keypoint-info">Strukturierter, wartbarer Code der Standards folgt.</p>
        </div>
        <div class="keypoint">
          <Terminal :size="16" class="keypoint-icon" />
          <p class="keypoint-title">Clean Code</p>
          <p class="keypoint-info">Strukturierter, wartbarer Code der Standards folgt.</p>
        </div>
        <div class="keypoint">
          <Terminal :size="16" class="keypoint-icon" />
          <p class="keypoint-title">Clean Code</p>
          <p class="keypoint-info">Strukturierter, wartbarer Code der Standards folgt.</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
  import { Terminal } from 'lucide-vue-next'
</script>

<style scoped>
  .aboutme {
    display: grid;
    grid-template-columns: 1fr 1fr;
    width: 100%;
    height: 100vh;
  }

  .aboutme-section1 {
    display: flex;
    flex-direction: column;
    align-items: start;
    justify-content: center;
    padding: 4rem;
  }

  .aboutme-section2 {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  .aboutme-section-info {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    color: var(--accent);
    gap: 0.5rem;
    font-family: var(--font-mono);
    font-size: 0.7rem;
  }

  .aboutme-question {
    font-family: var(--font-main);
    font-weight: 700;
    font-size: 2rem;
  }

  .aboutme-studio-name {
    color: var(--accent);
  }

  .aboutme-question-answer {
    color: var(--text-secondary);
  }

  .aboutme-developer-name {
    color: var(--text-primary);
  }

  .aboutme-stats {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: start;
    gap: 0.5rem;
    width: 100%;
  }

  .aboutme-stats-field {
    display: flex;
    position: relative;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    flex: 1;
    height: 82px;
    background: var(--bg-elevated);
    border: 1px solid var(--border-hover);
    padding: 0;
    margin: 0;
    gap: 1rem;
  }

  .stat-value {
    font-family: var(--font-main);
    font-size: 1.5rem;
    font-weight: 800;
    color: var(--text-primary);
    margin: 0;
  }

  .stat-text {
    font-family: var(--font-main);
    font-size: 0.6rem;
    color: var(--text-tertiary);
    white-space: nowrap;
    margin: 0;
  }

  .aboutme-keypoints {
    display: grid;
    grid-template-columns: 1fr 1fr;
    align-items: center;
    justify-content: center;
    padding: 4rem;
    gap: 2rem;
  }

  .keypoint {
    display: flex;
    flex-direction: column;
    align-items: start;
    justify-content: center;
    background: var(--bg-elevated);
    border: 1px solid var(--border-hover);
    padding: 1.5rem;
    gap: 0.8rem;
  }

  .keypoint-icon {
    color: var(--accent);
  }

  .keypoint-title {
    color: var(--text-primary);
    font-size: 1rem;
    font-weight: 600;
    margin: 0;
    padding: 0;
  }

  .keypoint-info {
    color: var(--text-tertiary);
    font-size: 0.8rem;
    margin: 0;
    padding: 0;
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