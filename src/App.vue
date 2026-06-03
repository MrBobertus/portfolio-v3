<template>
  <div class="noise-overlay" />
  <div>
    <NavBar @scroll-to-aboutme="scrollToAboutMe" @scroll-to-skills="scrollToSkills" @scroll-to-projects="scrollToProjects" @scroll-to-contact="scrollToContact" />
    <HeroSection class="animate-on-scroll" @scroll-to-projects="scrollToProjects" @scroll-to-contact="scrollToContact" />
    <AboutSection class="animate-on-scroll" ref="aboutmeRef" />
    <SkillsSection class="animate-on-scroll" ref="skillsRef" />
    <ProjectsSection class="animate-on-scroll" ref="projectsRef" />
    <ContactSection class="animate-on-scroll" ref="contactRef" />
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

import { ref, onMounted } from 'vue'

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

onMounted(() => {
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.classList.add('visible')
        observer.unobserve(entry.target)
      }
    })
  }, { threshold: 0.15 })

  document.querySelectorAll('.animate-on-scroll').forEach(el => {
    observer.observe(el)
  })
})
</script>

<style>
body {
  background-color: var(--bg-primary);
  color: var(--text-primary);
  font-family: var(--font-main);
  margin: 0;
  padding: 0;
}

.animate-on-scroll {
  opacity: 0;
  transform: translateY(30px);
  transition: opacity 0.6s ease, transform 0.6s ease;
}

.animate-on-scroll.visible {
  opacity: 1;
  transform: translateY(0);
}
</style>