<template>
  <Navbar />
  <Home />
  <About />
  <SkillsView/>
  <Timeline />
</template>
  
<script setup>
import Navbar from './components/Navbar.vue';
import Home from './components/HomeView.vue';
import About from './components/AboutView.vue';
import SkillsView from './components/SkillsView.vue';
import Timeline from './components/Timeline.vue';
</script>
  
<style>
* {
  font-family: 'Playfair Display', serif;
  color: black;
  overflow-x: hidden;
}

section {
  min-height: 100vh;
}
</style>