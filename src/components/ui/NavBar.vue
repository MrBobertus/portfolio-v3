<template>
  <div id="navbar" class="navbar" :class="{ 'menu-open': isMenuOpen }" style="transform: translateY(-100px);">
    <div class="navbar-brand-section">
      <div class="logo" role="img" aria-label="MRB Labs Logo"></div>
      <div class="navbar-vertical">
        <p class="title">MRB Labs</p>
        <p class="tertiary-text">Entwicklung. Innovation. Präzision.</p>
      </div>
    </div>

    <button @click="toggleMenu" class="menu-toggle-btn" aria-label="Menü öffnen">
      <Menu v-if="!isMenuOpen" :size="20" />
      <X v-else :size="20" />
    </button>

    <nav class="navbar-links" :class="{ 'is-open': isMenuOpen }">
      <button @click="navigate('scroll-to-aboutme')" class="secondary-text">01 // Über mich</button>
      <button @click="navigate('scroll-to-skills')" class="secondary-text">02 // Skills</button>
      <button @click="navigate('scroll-to-projects')" class="secondary-text">03 // Projekte</button>
      <button @click="navigate('scroll-to-contact')" class="secondary-text">04 // Kontakt</button>
    </nav>
  </div>
</template>

<script setup>
  import { ref, onMounted } from 'vue'
  import { Menu, X } from 'lucide-vue-next'

  const emit = defineEmits(['scroll-to-aboutme','scroll-to-skills','scroll-to-projects','scroll-to-contact'])
  
  const isMenuOpen = ref(false)

  const toggleMenu = () => {
    isMenuOpen.value = !isMenuOpen.value
  }

  const navigate = (event) => {
    isMenuOpen.value = false
    emit(event)
  }

  onMounted(() => {
    const navbar = document.getElementById("navbar")
    setTimeout(() => {
      navbar.style.transform = 'translateY(0)';
    }, 200);
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
  position: fixed !important;
  top: 0 !important;
  left: 0 !important;
  right: 0 !important;
  width: 100vw !important;
  box-sizing: border-box !important;
  margin: 0 !important;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 2rem;
  z-index: 99;
  mask: linear-gradient(black, black, transparent);
  backdrop-filter: blur(5px) brightness(0.5);
  transition: transform 0.5s ease;
}

.navbar.menu-open {
  mask: none !important;
  -webkit-mask: none !important;
  background-color: transparent !important;
  backdrop-filter: none !important;
}

.navbar-brand-section {
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

.navbar-links {
  display: flex;
  flex-direction: row;
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

.menu-toggle-btn {
  display: none;
}

@media (max-width: 768px) {
  .navbar {
    padding: 0.8rem 1.5rem;
  }

  .logo {
    width: 38px;
    height: 38px;
  }

  .title {
    font-size: 1.1rem;
  }

  .tertiary-text {
    display: none !important;
  }

  .menu-toggle-btn {
    display: block;
    background: none;
    border: none;
    color: var(--text-primary);
    cursor: pointer;
    padding: 0.5rem;
    z-index: 100;
    position: relative;
  }

  .navbar-brand-section {
    z-index: 100;
    position: relative;
  }

  .navbar-links {
    display: none;
  }

  .navbar-links.is-open {
    display: flex;
    position: fixed;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
    background-color: rgba(10, 10, 10, 0.75) !important;
    backdrop-filter: blur(4px) !important;
    -webkit-backdrop-filter: blur(4px) !important;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 2rem;
    z-index: 98;
  }

  .navbar-links button {
    font-size: 1.5rem;
    width: auto;
    text-align: center;
    padding: 0.5rem 1rem;
  }
}
</style>