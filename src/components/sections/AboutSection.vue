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
          Ich bin <span class="aboutme-developer-name">MrBobertus</span>, ein Entwickler mit Leidenschaft für kreative und praktische Lösungen. Mit MRB Labs habe ich einen Ort geschaffen, an dem Ideen nicht nur Konzepte bleiben, sondern zu echten Projekten werden.
        </p>

        <p>
          Besonders wichtig sind mir Anpassungsfähigkeit, die Bereitschaft ständig Neues zu lernen und die Motivation, mich immer weiterzuentwickeln. Viele meiner Fähigkeiten habe ich mir durch eigene Projekte angeeignet, von kleinen Experimenten bis hin zu größeren Anwendungen wie diesem Portfolio, das vollständig ohne KI-generierten Code entwickelt wurde.
        </p>

        <p>
          Für mich ist Entwicklung ein kontinuierlicher Prozess. Herausforderungen gehören dazu, Fehler ebenso. Statt daran zu scheitern, nutze ich sie als Möglichkeit, besser zu werden und neue Wege zu entdecken. Mit genügend Neugier, Ausdauer und Zeit lassen sich oft Lösungen finden, die anfangs unmöglich wirken.
        </p>
        <strong>"Ideen sind nur der Anfang. Erst durch Ausprobieren, Fehler und Verbesserungen werden sie Realität." ~ich</strong>
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
          <Lightbulb :size="16" class="keypoint-icon" />
          <p class="keypoint-title">Ideen umsetzen</p>
          <p class="keypoint-info">
            Gute Ideen haben viele. Ich glaube daran, sie tatsächlich zu bauen.
          </p>
        </div>
        <div class="keypoint">
          <Rocket :size="16" class="keypoint-icon" />
          <p class="keypoint-title">Ständig lernen</p>
          <p class="keypoint-info">
            Jede neue Technologie ist eine Chance, etwas Neues zu entdecken.
          </p>
        </div>
        <div class="keypoint">
          <Wrench :size="16" class="keypoint-icon" />
          <p class="keypoint-title">Probleme lösen</p>
          <p class="keypoint-info">
            Entwicklung bedeutet für mich, Herausforderungen in Lösungen zu verwandeln.
          </p>
        </div>
        <div class="keypoint">
          <TrendingUp :size="16" class="keypoint-icon" />
          <p class="keypoint-title">Kontinuierliche Verbesserung</p>
          <p class="keypoint-info">
            Fehler sind kein Rückschritt, sondern Teil des Fortschritts.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
  import { Lightbulb,Rocket,Wrench,TrendingUp } from 'lucide-vue-next'
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
    margin: 0;
  }

  .aboutme-studio-name {
    color: var(--accent);
  }

  .aboutme-question-answer {
    color: var(--text-secondary);
    margin-top: 2rem;
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
    margin-top: 2rem;
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
    transition: all 0.4s ease;
  }

  .aboutme-stats-field:has(+ .aboutme-stats-field:hover) {
    transform: scale(1.06);
    z-index: 9;
  }

  .aboutme-stats:hover .aboutme-stats-field:hover {
    transform: scale(1.2);
    z-index: 99;
  }

  .aboutme-stats-field:hover + .aboutme-stats-field {
    transform: scale(1.06);
    z-index: 9;
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
    padding: 2rem;
    gap: 0.8rem;
    transition: all 0.4s ease;
  }
  
  .keypoint:hover {
    background: var(--bg-secondary);
    border: 1px solid var(--border);
    transform: scale(1.1);
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

  @media (max-width: 768px) {
    .aboutme {
      grid-template-columns: 1fr;
      height: auto;
    }

    .aboutme-section1 {
      padding: 3rem 1.5rem;
    }

    .aboutme-stats {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 1rem;
    }

    .aboutme-stats-field:hover,
    .aboutme-stats:hover .aboutme-stats-field:hover,
    .aboutme-stats-field:has(+ .aboutme-stats-field:hover),
    .aboutme-stats-field:hover + .aboutme-stats-field {
      transform: none !important;
    }

    .aboutme-keypoints {
      grid-template-columns: 1fr;
      padding: 1.5rem;
      gap: 1.5rem;
    }

    .keypoint:hover {
      transform: none !important;
    }
  }
</style>