<template>
  <section class="connect-section">
    <h2>
      Let's <span class="highlight" style="margin-right: 7px;">connect</span>there
    </h2>
    <div class="socials">
      <a v-for="item in socialLinks" :key="item.name" :href="item.url" target="_blank" class="card" style="text-decoration: none;">
        <div class="left">
          <strong>{{ item.name }}</strong>
          <p>{{ item.desc }}</p>
        </div>
        <img :src="item.icon" :alt="item.name" />
      </a>
    </div>

    <footer class="footer">
      <p>Copyright © 2025 Amelia all rights reserved </p>
    </footer>
  </section>
</template>

<script>
import { instagram, facebook, whatsapp, linkedin } from './icons';

export default {
  name: 'ConnectSection',
  data() {
    return {
      socialLinks: [
        {
          name: 'Instagram',
          desc: 'Social media profile',
          icon: instagram,
          url: 'https://www.instagram.com/melliaptrri'
        },
        {
          name: 'Facebook',
          desc: 'Social media profile',
          icon: facebook,
          url: 'https://www.facebook.com/Amelia Putri Saparani'
        },
        {
          name: 'Whatsapp',
          desc: 'For fast response',
          icon: whatsapp,
          url: 'https://wa.me/6289530294376'
        },
        {
          name: 'Linkedin',
          desc: 'Network profile',
          icon: linkedin,
          url: 'https://www.linkedin.com/in/Amelia Putri'
        }
      ]
    };
  }
}
</script>

<style scoped>
.connect-section{
    background: #F0E4D3;
    padding: 60px 40px;
    text-align: center;
}

.connect-section h2{
    font-size: 24px;
    margin-bottom: 30px;
    font-family: poppins;
    color: black;
    font-weight: bold;
}

.connect-section .highlight{
    color: #D9A299;
    font-family: 'Oleo Script Swash Caps', cursive;
}

.socials{
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));
    gap: 20px;
    margin-bottom: 50px;
    justify-items: center;
    color: black;
    font-weight: bold;
}

.card{
    background-color: #d9d9d9;
    padding: 15px 20px;
    border-radius: 8px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 280px;
    text-align: left;
    color: black;
    font-weight: bold;
}


.card .left p{
    font-size: 13px;
    color: #555;
    margin-top: 5px;
     text-decoration: none;
     color: inherit;
}

.card img{
    width: 32px;
    height: 32px;
}

.footer{
    border-top: 1px solid #aaa;
    padding-top: 30px;
}

.footer p{
    font-size: 13px;
    color: black;
}

@media (max-width: 768px) {
  .connect-section {
    padding: 40px 20px;
  }

  .connect-section h2 {
    font-size: 20px;
  }

  .socials {
    grid-template-columns: repeat(1, 1fr); /* jadi 1 kolom di HP */
    gap: 16px;
  }

  .card {
    width: 100%;
    max-width: 300px;
    flex-direction: row;
    justify-content: space-between;
  }

  .card img {
    width: 28px;
    height: 28px;
  }

  .card .left strong {
    font-size: 14px;
  }

  .card .left p {
    font-size: 12px;
  }

  .footer p {
    font-size: 12px;
  }
}

</style>