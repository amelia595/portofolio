<template>
    <section class="contact-section">
        <div class="contact-form">
            <input type="text" v-model="name" placeholder="Your name" />
<input type="email" v-model="email" placeholder="Your email" />
<textarea rows="4" v-model="detail" placeholder="Detail"></textarea>
            <button @click="sendViaWhatsApp">Send Message</button>
        </div>

        <div class="contact-text">
            <h2>
                Let's <span class="italic" style="margin-right: 8px;">talk</span>for<br/>
                something <span class="highlight">special</span>
            </h2>
            <p>Jangan ragu untuk menghubungi saya jika ada projek, ide, atau sekadar ingin berdiskusi</p>
            <a href="mailto:Amelputri8866@gmail.com" class="email">Amelputri8866@gmail.com</a>
        </div>
    </section>
</template>

<script>
export default {
  data() {
    return {
      name: '',
      email: '',
      detail: ''
    };
  },
  methods: {
    sendViaWhatsApp() {
      const name = this.name;
      const email = this.email;
      const detail = this.detail;

      const message = `Halo Amelia!%0ANama: ${name}%0AEmail: ${email}%0ADetail: ${detail}`;
      const whatsappLink = `https://wa.me/6289530294376?text=${message}`;
      window.open(whatsappLink, '_blank');
    }
  }
};
</script>

<style scoped>
.contact-section{
    display: flex;
    justify-content: space-between;
    padding: 60px 40px;
    background-color: #FAF7F3;
    flex-wrap: wrap;
    gap: 40px;
}

.contact-form{
    flex: 1;
    display: flex;
    flex-direction: column;
    gap:20px;
    max-width: 400px;
    
}

.contact-form input,
.contact-form textarea{
    padding: 12px;
    border: 1px solid #6B6B6B;
    border-radius: 4px;
    font-family: poppins;
    font-size: 14px;
    margin-left: 50px;
}

.contact-form button{
    width: fit-content;
    padding: 10px 20px;
    background-color: #DCC5B2;
    border: none;
    border-radius: 8px;
    cursor: pointer;
    font-family: poppins;
    margin-left: 50px;
}

.contact-text{
    flex: 1;
    max-width: 500px;
    color: black;
}

.contact-text h2{
    font-size: 24px;
    line-height: 1.4;
    margin-bottom: 10px;
    font-weight: bold;
    word-spacing: 3px;
}

.contact-text .italic{
    font-family: 'Oleo Script Swash Caps', cursive;
    color: #D9A299;
    font-weight: bold;
}

.contact-text .highlight{
    font-family: 'Oleo Script Swash Caps', cursive;
    color:  #D9A299;
    font-weight: bold;

}

.contact-text p{
    color: #918E8E;
    margin-bottom: 15px;
    margin-right: 80px;
    word-spacing: 1px;
}

.contact-text .email{
    color: #D9A299;
    font-weight: bold;
    text-decoration: none;
}

</style>