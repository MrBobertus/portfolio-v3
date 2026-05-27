<template>
  <div class="aboutme">
    <div class="aboutme-section1">
      <p>01 // ÜBER MICH</p>
      <p>Wer steckt hinter <span>MRB Labs</span>?</p>
      <div>
        <p>
              Ich bin <span>MrBobertus</span>, ein leidenschaftlicher
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
        <div>
          <div class="box-top-left"></div>
          <div class="box-bottom-right"></div>
          <p>2+</p>
          <p>JAHRE ERFAHRUNG</p>
        </div>
        <div>
          <div class="box-top-left"></div>
          <div class="box-bottom-right"></div>
          <p>4+</p>
          <p>PROJEKTE</p>
        </div>
        <div>
          <div class="box-top-left"></div>
          <div class="box-bottom-right"></div>
          <p>7+</p>
          <p>TECHNOLOGIEN</p>
        </div>
        <div>
          <div class="box-top-left"></div>
          <div class="box-bottom-right"></div>
          <p>3+</p>
          <p>KUNDEN</p>
        </div>
      </div>
    </div>
    <div class="aboutme-section2">
      <div class="aboutme-keypoints">
        <div>
          <p>Clean Code</p>
          <p></p>
        </div>
        <div>
          <p>Performance</p>
          <p></p>
        </div>
        <div>
          <p>Architektur</p>
          <p></p>
        </div>
        <div>
          <p>Innovation</p>
          <p></p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
</script>

<style scoped>
  .aboutme {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 2rem;
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

  .aboutme-stats {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    padding: 4rem;
  }

  .aboutme-section2 {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  .aboutme-keypoints {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 2rem;
  }
</style>