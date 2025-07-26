<template>
    <section class="certifications-section">
        <h2 class="section-title">
            Let's have a look at <br/>
            <span class="highlight">my</span>
            <span class="script-font" style="margin-left: 7px;">certifications</span>
        </h2>
        <p class="description">
            Sertifikat yang saya dapat selama proses belajar dan pengembangan skill
        </p>

        <div class="cert-grid">
            <div v-for="(cert, index) in certificates" :key="index" class="cert-card">
                <img :src="cert.image" :alt="cert.title"/>
                <p class="cert-title">{{ cert.title }}</p>
            </div>
        </div>

        <button class="more-btn">More</button>
    </section>
</template>

<script>
import { g14, g15, g16, g17, g18, g19, g20 } from '@/assets/image';

export default {
    name: 'Certifications' ,
    data() {
        return {
            certificates: [
                { title: 'Lomba Web Dev', image: g16},
                { title: 'Belajar Vue.Js', image: g14},
                { title: 'Belajar UI/UX', image: g15},
            ]
        }
    }
}
</script>

<style scoped>
.certifications-section {
    text-align: center;
    padding: 60px 40px;
    background-color: #FAF7F3;
}

.section-title{
    font-size: 24px;
    margin-bottom: 10px;
    font-weight: 600;
    color: black;
    font-weight: bold;
}

.highlight{
    font-weight: bold;
    font-size: 24px;
    gap: 10px;
}

.script-font{
    font-family: 'Oleo Script Swash Caps', cursive;
    color: #D9A299;
    font-weight: bold;
}

.description{
    font-size: 14px;
    color: #918E8E;
    margin-bottom: 40px;
}

.cert-grid{
    display: flex;
    gap: 50px;
    justify-content: center;
    flex-wrap: wrap;
    margin-bottom: 30px;
}

.cert-card{
    width: 240px;
    background-color: #F0E4D3;
    overflow: hidden;
    box-shadow: 0 4px 10px rgba(0,0,0,0.05);
    height: 155px;
    color: black;
    font-size: 16px;
}

.cert-card img{
    width: 100%;
    height: auto;
    object-fit: cover;
}

.cert.title{
    font-size: 14px;
    padding: 10px;
    font-weight: 500;
}

.more-btn{
    background-color: #DCC5B2;
    border: none;
    padding: 10px 20px;
    border-radius: 6px;
    cursor: pointer;
    font-family: poppins;
}
</style>