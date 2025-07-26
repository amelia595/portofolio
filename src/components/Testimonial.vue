<template>
    <section class="testimonial-section">
        <h2 class="title">Comments From <strong style="font-weight: bold;">My Friends</strong></h2>
        <p class="desc">
            Berikut beberapa kesan dan 
            komentar dari orang-orang yang 
            pernah melihat karya atau desain saya
        </p>

        <div class="testimonial-grid">
            <div class="card" v-for="(item, i) in comments" :key="i">
                <p class="comment">{{ item.text }}</p>
                <div class="profile">
                    <div class="avatar"></div>
                    <div class="info">
                        <p class="name">{{ item.name }}</p>
                        <p class="role">{{ item.role }}</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Testimonial',
    data() {
        return {
            comments: [
                {
                    text:'Codingan Vue kamu udah oke, tinggal latihan terus biar makin lancar yaa',
                    name:'Ikhsan',
                    role:''
                },
                {
                    text:'Keren Amel, Gak nyangka udah bisa bikin web begini',
                    name:'Ahmad',
                    role:''
                },
                {
                    text:'Desain kamu rapi dan enak dilihat, kayaknya cocok banget buat aplikasi beneran',
                    name:'Ayu',
                    role:''
                }
            ]
        }
    }
}
</script>

<style scoped>
.testimonial-section{
    padding: 60px 40px;
    background-color: #F0E4D3;
    text-align: center;
}

.title{
    font-size: 22px;
    margin-bottom: 8px;
    color: black;
    font-weight: bold;
    font-family: poppins;
    margin-right: 890px;
}

.desc{
    font-size: 14px;
    color: grey;
    margin-bottom: 40px;
    line-height: 1.7;
    margin-right: 549px;
    margin-left: 31px;
    text-align: left;
}

.testimonial-grid{
    display:flex;
    gap: 50px;
    justify-content: center;
    flex-wrap: wrap;
}

.card{
    background-color: #FAF7F3;
    border-radius: 8px;
    padding: 20px;
    width: 260px;
    box-shadow: 0 4px 12px rgba(0,0,0,0.05);
    text-align: left;
    display:flex;
    flex-direction: column;
    justify-content: space-between;
    height: 220px;
}

.profile{
    display: flex;
    align-items: center;
    gap: 10px;
    
}

.avatar{
    width: 28px;
    height: 28px;
    background-color: #aaa;
    border-radius: 50%;
    margin-top: 20px;
}

.info .name{
    font-size: 13px;
    font-weight: bold;
    color: black;
    margin-top: 20px;
}

.info .role{
    font-size: 10px;
    color: #666;
}

@media (max-width: 768px) {
  .testimonial-section {
    padding: 40px 20px;
  }

  .title {
    font-size: 20px;
    margin-right: 0;
    text-align: center;
  }

  .desc {
    margin: 0 auto 30px auto;
    font-size: 13px;
    text-align: center;
    max-width: 100%;
    line-height: 1.6;
  }

  .testimonial-grid {
    flex-direction: column;
    align-items: center;
    gap: 20px;
  }

  .card {
    width: 100%;
    max-width: 320px;
    height: auto;
  }

  .comment {
    font-size: 14px;
  }

  .info .name {
    font-size: 13px;
  }

  .info .role {
    font-size: 10px;
  }
}

</style>