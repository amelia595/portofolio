<script setup>
import Header from './components/Header.vue';
import ProjectList from './components/ProjectList.vue';
import Tech from './components/Tech.vue';
import Ido from './components/Ido.vue';
import Cerftifi from './components/Cerftifi.vue';
import Testimonial from './components/Testimonial.vue';
import Contact from './components/Contact.vue';
import Connect from './components/Connect.vue';
</script>



<template>
  <section id="Home"><Header /></section>
  <RouterView />
  <secion id="About">
   <ProjectList/>
   <Tech/>
  </secion>
  <section id="Project">
   <Ido/>
  <Cerftifi/>
  </section>
  <Testimonial/>
  <section id="Contact"><Contact /></section>
  <Connect/>
</template>