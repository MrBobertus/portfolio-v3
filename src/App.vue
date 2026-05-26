<template>
  <div class="noise-overlay"/>
  <div>
    <NavBar />
    <HeroSection />
    <AboutSection />
    <SkillsSection />
    <ProjectsSection />
    <ContactSection />
    <FooterBar />
  </div>
</template>

<script setup>
import NavBar from './components/ui/NavBar.vue'
import FooterBar from './components/ui/FooterBar.vue'
import HeroSection from './components/sections/HeroSection.vue'
import AboutSection from './components/sections/AboutSection.vue'
import SkillsSection from './components/sections/SkillsSection.vue'
import ProjectsSection from './components/sections/ProjectsSection.vue'
import ContactSection from './components/sections/ContactSection.vue'
</script>

<style>
body {
  background-color: var(--bg-primary);
  color: var(--text-primary);
  font-family: var(--font-main);
  margin: 0;
  padding: 0;
}
</style>