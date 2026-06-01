<template>
  <div class="footer">
    <div class="footer-info">
      <div class="logo" role="img" aria-label="MRB Labs Logo"></div>
      <p class="footer-studio-name">MRB Labs</p>
      <p class="footer-copyright"><Copyright class="footer-copyright-symbole" size="12" />2026 MrBobertus</p>
    </div>
    <button @click="scrollToTop" class="footer-button-totop">ZURÜCK NACH OBEN 
      <div class="footer-button-totop-div">
        <ArrowUp size="14" />
      </div>
    </button>
  </div>
</template>

<script setup>
  import { ArrowUp, Copyright } from 'lucide-vue-next'

  const scrollToTop = () => {
    window.scrollTo({ top: 0, behavior: "smooth" });
  }
</script>

<style scoped>
.footer-studio-name {
  color: var(--text-primary);
  font-size: 1rem;
  font-weight: 600;
  font-family: var(--font-main);
  margin: 0;
  padding: 0;
}

.footer-copyright {
  display: flex;
  align-items: center;
  justify-content: center;
  color: var(--text-tertiary);
  font-size: 0.7rem;
  font-family: var(--font-mono);
  margin: 0;
  padding: 0;
}

.footer-copyright-symbole {
  font-size: 1rem;
  margin-right: 0.1rem;
  text-align: center;
}

.footer-button-totop {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  background: none;
  border: none;
  color: var(--text-tertiary);
  font-size: 0.7rem;
  text-align: center;
  font-family: var(--font-main);
  margin: 0;
  padding: 0.5rem;
  transition: all 0.2s ease;
}

.footer-button-totop:hover {
  cursor: pointer;
  color: var(--accent-light)

}

.footer-button-totop-div {
  display: flex;
  align-items: center;
  justify-content: center;
  border: 1px solid var(--bg-elevated);
  margin: 0 0 0 0.5rem;
  padding: 0.1rem;
}

.footer {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 2rem;
}

.footer-info {
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 0.4rem;
}

.logo {
  width: 42px;
  height: 42px;
  padding: 0;
  margin: 0;
  background-color: var(--accent-light); 
  mask: url(../../assets/logo.svg) no-repeat center / contain;
}
</style>