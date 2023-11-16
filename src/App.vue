<template>
<Navbar/>
<Home/>
<About/>
<Timeline/>
<Testimonials/>
<Projects/>
</template>

<script setup>
import Navbar from './components/Navbar.vue';
import Home from './components/HomeView.vue';
import About from './components/AboutView.vue';
import Timeline from './components/Timeline.vue';
import Testimonials from './components/TestimonialsView.vue'
import Projects from './components/ProjectsView.vue';
</script>

<style>
@font-face {
  font-family: 'Tokyo2097';
  src: url('./assets/Tokyo2097-7RYP.ttf') format('truetype');
  font-weight: normal;
  font-style: normal;
}

* {
  font-family: 'Tokyo2097', sans-serif;
  color: white;
  overflow-x: hidden;
}

section{
  min-height: 100vh;
}


</style>