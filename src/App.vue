<template>
  <div class="noise-overlay" />
  <div>
    <NavBar @scroll-to-aboutme="scrollToAboutMe" @scroll-to-skills="scrollToSkills" @scroll-to-projects="scrollToProjects" @scroll-to-contact="scrollToContact" />
    <HeroSection @scroll-to-projects="scrollToProjects" @scroll-to-contact="scrollToContact" />
    <AboutSection ref="aboutmeRef" />
    <SkillsSection ref="skillsRef" />
    <ProjectsSection ref="projectsRef" />
    <ContactSection ref="contactRef" />
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

import { ref } from 'vue'

const aboutmeRef = ref(null)
const skillsRef = ref(null)
const projectsRef = ref(null)
const contactRef = ref(null)

const scrollToAboutMe = () => {
  aboutmeRef.value.$el.scrollIntoView({ behavior: 'smooth' })
}

const scrollToSkills = () => {
  skillsRef.value.$el.scrollIntoView({ behavior: 'smooth' })
}

const scrollToProjects = () => {
  projectsRef.value.$el.scrollIntoView({ behavior: 'smooth' })
}

const scrollToContact = () => {
  contactRef.value.$el.scrollIntoView({ behavior: 'smooth' })
}
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