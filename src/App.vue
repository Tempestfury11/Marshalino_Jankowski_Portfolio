<template>
  <Navbar />
  <Home />
  <About />
  <Skills/>
  <Timeline />
  <Testimonials/>
  <ProjectsView/>
</template>
  
<script setup>
import Navbar from './components/Navbar.vue';
import Home from './components/HomeView.vue';
import About from './components/AboutView.vue';
import Skills from './components/SkillsView.vue';
import Timeline from './components/Timeline.vue';
import Testimonials from './components/TestimonialsView.vue';
import ProjectsView from './components/ProjectsView.vue';
</script>
  
<style>
* {
  font-family: 'Playfair Display', serif;
  color: black;
}

section {
  min-height: 100vh;
}
</style>