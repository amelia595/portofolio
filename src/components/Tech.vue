<script setup>

</script>

<template>
    <section class="skills-section">
     <div class="skills-text">
        <h3>Skills <span class="highlight-tech" style="margin-top:20px">&amp; Tech</span>
        Stack</h3>
        <p>Berikut adalah tools dan teknologi yang saya gunakan
        saat belajar dan membuat projek</p>
       
     </div>
     
     <div class="tech-grid">
        <img src="@/assets/image/gambarvue2.jpg"/>
        <img src="@/assets/image/gambarvs3.jpg"/>
        <img src="@/assets/image/gambarsql4.jpg"/>
        <img src="@/assets/image/gambargit5.jpg"/>
        <img src="@/assets/image/gambarhtml6.jpg"/>
        <img src="@/assets/image/gambarcss7.jpg"/>
        <img src="@/assets/image/gambarjs8.jpg"/>
        <img src="@/assets/image/gambarphp9.jpg"/>
        <img src="@/assets/image/gambarfig10.jpg"/>
        <img src="@/assets/image/gambar24.jpg"/>
        <img src="@/assets/image/gambar25.jpg"/>
        <img src="@/assets/image/gambar26.jpg"/>
     </div>
    </section>
</template>

<style scoped>
.skills-section{
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    padding: 60px 40px;
    flex-wrap: wrap;
    gap: 40px;
}

.skills-text{
    max-width: 400px;
    padding-top: 20px;
}

.skills-text h3{
    font-size: 22px;
    font-weight: bold;
    color: black;
    word-spacing: 5px;
    padding-top: 90px;
    margin-left: 50px;
}

.highlight-tech{
    color: #D9A299;
    font-family: 'Oleo Script Swash Caps', cursive;
}

.skills-text p{
    color: black;
    margin-bottom: 20px;
    margin-left: 250px;
    margin: 20px -0;
    max-width: 400px;
    padding-left: 50px;
    padding-top: -5px;
}



.tech-grid{
    display: grid;
    grid-template-columns: repeat(4, 100px);
    gap: 30px;
    justify-content: center;
    align-items: center;
    margin-right: 150px;
    
}

.tech-grid img{
    width: 100px;
    height: 100px;
    object-fit: contain;
    background: white;
    border-radius: 12px;
    box-shadow: 0 4px 8px rgba(0,0,0,0.05);
    padding: 10px;
    border-bottom: 4px solid #d9cfc0;
}

@media (max-width: 768px) {
  .skills-section {
    flex-direction: column;
    align-items: center;
    padding: 40px 20px;
  }

  .skills-text {
    max-width: 100%;
    text-align: center;
  }

  .skills-text h3,
  .skills-text p,
  .more-btn {
    margin-left: 0;
  }

  .skills-text h3 {
    font-size: 20px;
    margin-top: 20px;
  }

  .skills-text p {
    font-size: 14px;
  }

  .more-btn {
    margin-top: 10px;
  }

  .tech-grid {
    grid-template-columns: repeat(3, 1fr); 
    gap: 20px;
    margin: 40px 0 0 0;
  }

  .tech-grid img {
    width: 100%;
    max-width: 100px;
    height: auto;
  }
}

</style>