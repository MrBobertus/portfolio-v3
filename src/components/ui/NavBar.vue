<template>
  <div id="navbar" class="navbar" style="transform: translateY(-100px);">
    <div class="navbar-horizontal">
      <div class="logo" role="img" aria-label="MRB Labs Logo"></div>
      <div class="navbar-vertical">
        <p class="title">MRB Labs</p>
        <p class="tertiary-text">Entwicklung. Innovation. Präzision.</p>
      </div>
    </div>
    <nav class="navbar-horizontal">
      <button @click="emit('scroll-to-aboutme')" class="secondary-text">01 // Über mich</button>
      <button @click="emit('scroll-to-skills')" class="secondary-text">02 // Skills</button>
      <button @click="emit('scroll-to-projects')" class="secondary-text">03 // Projekte</button>
      <button @click="emit('scroll-to-contact')" class="secondary-text">04 // Kontakt</button>
    </nav>
  </div>
</template>

<script setup>
  import { ref, onMounted } from 'vue'
  import { Terminal, Mouse } from 'lucide-vue-next'

  const emit = defineEmits(['scroll-to-aboutme','scroll-to-skills','scroll-to-projects','scroll-to-contact'])

  onMounted(() => {
    const navbar = document.getElementById("navbar")

    const showNavbar = () => {
      setTimeout(() => {
        navbar.style.transform = 'translateY(0)';
      }, 200);
    }
    
    showNavbar()
  })
</script>

<style scoped>
.title {
  color: var(--text-primary);
  font-size: 1.2rem;
  text-align: left;
  font-family: var(--font-main);
  margin: 0;
  padding: 0;
}

.secondary-text {
  color: var(--text-secondary);
  font-family: var(--font-main);
  margin: 0;
  padding: 0;
}

.tertiary-text {
  color: var(--text-tertiary);
  font-size: 0.7rem;
  text-align: left;
  font-family: var(--font-main);
  margin: 0;
  padding: 0;
}

.navbar {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%; 
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 2rem;
  z-index:99;
  mask: linear-gradient(black, black, transparent);
  backdrop-filter: blur(5px) brightness(0.5);
  transition: all 0.5s ease;
}

.navbar-horizontal {
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 0;
}

.navbar-vertical {
  display: flex;
  flex-direction: column;
  align-items: start;
  gap: 0;
}

.logo {
  width: 50px;
  height: 50px;
  margin: 0 0.7rem 0 0;
  background-color: var(--accent-light); 
  mask: url(../../assets/logo.svg) no-repeat center / contain;
}

nav.navbar-horizontal {
  gap: 2rem;
}

nav button {
  background-color: transparent;
  border: none;
  word-spacing: 0.1rem;
  transition: color 0.5s ease-in-out; 
}

nav button:hover {
  color: var(--accent-light);
  cursor: pointer;
}
</style>