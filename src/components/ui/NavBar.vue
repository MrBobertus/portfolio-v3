<template>
  <div class="navbar">
    <div class="navbar-horizontal">
      <img class="logo" src="https://placehold.co/400" width="50" height="50" alt="MRB Labs Logo"/>
      <div class="navbar-vertical">
        <p class="title">MRB Labs</p>
        <p class="tertiary-text">DEV STUDIO</p>
      </div>
    </div>
    <nav class="navbar-horizontal">
      <button class="secondary-text">01 // Über mich</button>
      <button class="secondary-text">02 // Skills</button>
      <button class="secondary-text">03 // Projekte</button>
      <button class="secondary-text">04 // Kontakt</button>
    </nav>
  </div>
</template>

<script setup>
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
  margin: 0 0.7rem 0 0;
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