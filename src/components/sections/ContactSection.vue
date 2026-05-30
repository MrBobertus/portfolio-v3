<template>
  <div class="contact">
    <div class="contact-section-info">
      <div class="line"></div>
      <p>04 // KONTAKT</p>
    </div>
    <p class="contact-title">Irgendwelche <span class="contact-title-keyword">Fragen</span>?</p>
    <p class="contact-explanation">Hast du eine Frage im Kopf oder benötigtst du hilfe? Schreib mir, vielleicht kann ich ja helfen.</p>
    <div class="contact-container">
      <div class="contact-info">
        <div class="contact-box">
          <div class="box-top-left"></div>
          <div class="box-bottom-right"></div>
          <p class="contact-box-section"><Mail :size="22" />E-MAIL</p>
          <a href="mailto:mr.bobertus.dev@gmail.com" class="contact-box-title">mr.bobertus.dev@gmail.com<ArrowUpRight :size="16" /></a>
        </div>
        <div class="contact-box">
          <div class="box-top-left"></div>
          <div class="box-bottom-right"></div>
          <p class="contact-box-section"><Map :size="22" />STANDORT</p>
          <p class="contact-box-title">Deutschland</p>
          <p class="contact-box-info">Remote verfügbar</p>
        </div>
        <div class="contact-social-section">
          <p class="contact-social-section-title">SOCIALS</p>
          <div class="contact-social-list">
            <a class="contact-social">
              <p>Github</p>
              <ArrowUpRight :size="18" />
            </a>
            <a class="contact-social">
              <p>Youtube</p>
              <ArrowUpRight :size="18" />
            </a>
          </div>
        </div>
      </div>
      <div class="contact-section-formular">
        <form class="contact-formular">
          <div class="contact-data-inputs">
            <div class="contact-name-input">
              <label>NAME</label>
              <input placeholder="Max Mustermann" />
            </div>
            <div class="contact-email-input">
              <label>E-MAIL</label>
              <input placeholder="maxmustermann@mail.com" />
            </div>
          </div>
          <div class="contact-message-input">
            <label>Nachricht</label>
            <textarea rows="6" placeholder="Erzähle mir mehr von ..."></textarea>
          </div>
          <button class="button1"><Send :size="16" />NACHRICHT SENDEN</button>
        </form>
      </div>
    </div>
  </div>
</template>

<script setup>
  import { ArrowUpRight, Send, Mail, Map} from 'lucide-vue-next'
</script>

<style scoped>
  .contact {
    display: flex;
    flex-direction: column;
    align-items: start;
    justify-content: center;
    padding: 4rem;
    width: 100%;
    height: 100vh;
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

  .contact-container {
    display: grid;
    grid-template-columns: 1fr 1fr;
    width: 100%;
  }

  .contact-info {
    display: flex;
    flex-direction: column;
    align-items: start;
    justify-content: center;
    gap: 1.5rem;
  }

  .contact-box {
    display: flex;
    position: relative;
    flex-direction: column;
    align-items: start;
    justify-content: center;
    width: 100%;
    background: var(--bg-elevated);
    border: 1px solid var(--border-hover);
    padding: 1.2rem 1.8rem;
    margin: 0;
    gap: 0.5rem;
  }

  .contact-box-section {
    display: flex;
    align-items: center;
    gap: 0.5rem;
    font-family: var(--font-mono);
    font-size: 0.75rem;
    color: var(--text-tertiary);
    margin: 0;
  }

  .contact-box-title {
    display: flex;
    align-items: center;
    gap: 0.5rem;
    color: var(--text-primary);
    margin: 0;
  }

  .contact-box-info {
    color: var(--text-tertiary);
    font-size: 0.8rem;
    margin: 0;
  }

  .contact-social-section {
    display: flex;
    position: relative;
    flex-direction: column;
    align-items: start;
    justify-content: center;
    width: 100%;
    background: none;
    padding: 0;
    margin: 0;
    gap: 0;
  }

  .contact-social-section-title {
    color: var(--text-tertiary);
    font-size: 0.7rem;
    margin-top: 1rem;
    padding: 0;
  }

  .contact-social-list {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 100%;
    gap: 1rem;
  }

  .contact-social {
    display: flex;
    position: relative;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    width: 100%;
    background: var(--bg-elevated);
    border: 1px solid var(--border-hover);
    padding: 0.4rem 1.6rem;
    margin: 0;
    gap: 1rem;
  }

  .contact-social  {
    color: var(--text-secondary);
    font-size: 1rem;
    font-weight: 500;
  }

  .contact-section-formular {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 100%;
    height: 100%;
  }

  .contact-formular {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: start;
    width: 100%;
    height: 100%;
    gap: 2rem;
  }

  .contact-data-inputs {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    width: 80%;
    gap: 3rem;
  }

  .contact-name-input {
    display: flex;
    flex-direction: column;
    align-items: start;
    justify-content: center;
    flex: 1;
  }

  .contact-name-input label {
    font-family: var(--font-mono);
    color: var(--text-secondary);
    font-size: 0.8rem;
  }

  .contact-name-input input {
    display: flex;
    position: relative;
    flex-direction: column;
    align-items: start;
    justify-content: center;
    width: 100%;
    color: var(--text-primary);
    font-size: 1rem;
    background: var(--bg-elevated);
    border: 1px solid var(--border-hover);
    padding: 1.2rem 1.8rem;
    margin: 0;
    gap: 0.5rem;
  }

  .contact-email-input {
    display: flex;
    flex-direction: column;
    align-items: start;
    justify-content: center;
    flex: 1;
  }

  .contact-email-input label {
    font-family: var(--font-mono);
    color: var(--text-secondary);
    font-size: 0.8rem;
  }

  
  .contact-email-input input {
    display: flex;
    position: relative;
    flex-direction: column;
    align-items: start;
    justify-content: center;
    width: 100%;
    color: var(--text-primary);
    font-size: 1rem;
    background: var(--bg-elevated);
    border: 1px solid var(--border-hover);
    padding: 1.2rem 1.8rem;
    margin: 0;
    gap: 0.5rem;
  }
  
  .contact-message-input {
    display: flex;
    flex-direction: column;
    align-items: start;
    justify-content: center;
    width: 80%;
  }

  .contact-message-input label {
    font-family: var(--font-mono);
    color: var(--text-secondary);
    font-size: 0.8rem;
  }


  .contact-message-input textarea {
    display: flex;
    position: relative;
    flex-direction: column;
    align-items: start;
    justify-content: center;
    width: 100%;
    color: var(--text-primary);
    font-size: 1rem;
    background: var(--bg-elevated);
    border: 1px solid var(--border-hover);
    padding: 1.2rem 1.8rem;
    margin: 0;
    gap: 0.5rem;
    resize: vertical;
  }

  .button1 {
    display: flex;
    align-items: center;
    gap: 0.5rem;
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