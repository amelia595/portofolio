<script setup>
import Tech from '@/components/Tech.vue';
import ProjectList from '@/components/ProjectList.vue';
import Ido from '@/components/Ido.vue';
import Cerftifi from '@/components/Cerftifi.vue';
import Testimonial from '@/components/Testimonial.vue';
import Contact from '@/components/Contact.vue';
import Connect from '@/components/Connect.vue';
import {
  g1, g2, g3, g4, g5, g6, g7, g8, g9, g10, g11, g12, g13, g14, g15, g16, g17, g18, g19, g20
} 
  from '@/assets/image'

import { instagram, facebook, linkedin, whatsapp } from '@/components/icons';
</script>

<template>
 <div class="container">
  <section class="hero">
    <div class="hero-text">
      <h2>
  <span class="highlight1">Learning</span>&nbsp;
  <strong style="font-weight: bold;">Frontend Development</strong>&nbsp;<br/> 
  <strong style="font-weight: bold;">with a</strong>&nbsp;
  <span class="highlight2">Passion for</span>&nbsp;
  <strong style="font-weight: bold;">UI/UX Design</strong>&nbsp;
</h2>

      <p> Halo, saya Amelia Putri Saparani yang sedang belajar untuk menjadi seorang Frontend Developer dan Desainer UI/UX</p>
      <button class="hire-btn"><a href="#Contact">Hire Me</a></button>
    </div>
   <div class="hero-image">
  <div class="circle-top"></div>
  <div class="circle-bottom"></div>
  <img :src="g1" />
</div>

  </section>

  <section class="projects">
  <div class="projects-row">
    <h3>My <span class="recent">recent projects</span></h3>
    <div class="stats">
      <div class="ya3" style="color: #918E8E;"><strong class="ya2" style="color: black; font-weight: bold;">1+</strong><br />Frontend Layouts Built</div>
      <div class="ya3"><strong class="ya2">3+</strong><br />Personal Projects</div>
      <div class="ya3"><strong class="ya2">5+</strong><br />UI/UX Concepts Designed</div>
    </div>
  </div>
</section>
 </div>
</template>

<style scoped>

.ya3{
  color:#918E8E
}
.ya2{
  color: black;
  font-weight: bold;
}
.container{
  background-color: #F0E4D3;
  color: black;
  padding-bottom: 40px;
  padding-top: 75px;
}

.hero{
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 60px 40px;
  flex-wrap: wrap;
}

.hero-text{
  flex: 1;
  min-width: 280px;
  margin-right: 40px;
  padding-left: 20px;
  margin-left: 70px;
}

.hero-text h2{
  font-size: 24px;
  line-height: 1.4;
  margin-bottom: 20px;
  word-spacing: 2px;
  font-weight: bold;
}

.highlight1{
 font-family: oleo script swash caps;
  color: #D9A299;
  font-weight: 600;
}

.highlight2{
  font-family: oleo script swash caps;
  color: #D9A299;
  font-weight: 600;
}

.hero-text p{
  margin: 20px 0;
  max-width: 400px;
  margin-bottom: 20px;
  color: #918E8E;
}

.hire-btn {
  padding: 10px 20px;
  border: none;
  background-color: #DCC5B2;
  border-radius: 6px;
  cursor: pointer;
  font-family: poppins;
  font-weight: 600;
}

.hire-btn a{
  color: black;
  text-decoration: none;
  font-family: poppins;
  font-weight: 600;
}
.hero-image{
  position: relative;
  width: 280px;
  height: 320px;
  margin-top: 20px;
  display: flex;
  margin-right: 75px;
}

.circle-top,
.circle-bottom {
  position: absolute;
  width: 89%;
  height: 50%;
  background-color: #d7a89b;
  border-radius: 999px;
  left: 0;
  z-index: 1;
}

.circle-top {
  top: 0;
  border-bottom-left-radius: 0;
  border-bottom-right-radius: 0;
}

.circle-bottom {
  bottom: 0;
  border-top-left-radius: 0;
  border-top-right-radius: 0;
}

.hero-image img{
  position: absolute;
  top: 30%;
  left: 15%;
  transform: translate(-50%, -50%);
  width: 330px;
  height: auto;
  z-index: 2;
  object-fit: cover;
  margin-right: 200px;

}

.projects{
  padding: 40px;
  margin-left: 125px;
}

.projects-row {
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 20px;
  margin-left: 10%;
}

.projects h3{
  font-size: 18px;
  margin-bottom: 30px;
  margin: 0;
}

.recent{
  color:#D9A299;
  font-family: oleo script swash caps;
}

.stats{
  display: flex;
  gap: 51px;
  font-size: 16px;
  margin-right: 20%;
}

@media (max-width: 768px) {
  .hero {
    flex-direction: column;
    padding: 30px 20px;
    text-align: center;
  }

  .hero-text {
    margin: 0 auto;
    padding: 0;
  }

  .hero-text h2 {
    font-size: 20px;
  }

  .hero-text p {
    font-size: 14px;
    max-width: 100%;
  }

  .hire-btn {
    padding: 8px 16px;
  }

  .hero-image {
    margin: 30px auto 0;
    width: 220px;
    height: 280px;
  }

  .hero-image img {
    width: 230px;
    left: 23%;
    top: 47%;
    transform: translate(-50%, -50%);
  }

  .circle-top,
  .circle-bottom {
    width: 100%;
  }

  .projects {
    padding: 20px;
    margin-left: 0;
    text-align: center;
  }

  .projects-row {
    flex-direction: column;
    align-items: center;
    margin-left: 0;
  }

  .projects h3 {
    font-size: 16px;
  }

  .stats {
    flex-direction: column;
    gap: 20px;
    margin: 0;
    font-size: 14px;
  }
}

</style>
