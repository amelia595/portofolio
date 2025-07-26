<script setup>

</script>

<template>
    <section class="projects-list">
        <div class="project-card" v-for="(project, index) in projects" key="index">
            <img :src="project.image" :alt="project.tittle"/>
            <div class="project-info">
                <h4>{{ project.tittle }}</h4>
                <p>{{ project.type }}</p>
            </div>
            <div class="arrow-icon">
                <span>↗</span>
            </div>
        </div>
    </section>
</template>

<script>
    import {g11, g12, g13} from '@/assets/image'

    export default {
        name: 'ProjectList',
        data(){
            return{
                projects: [
                    {
                        tittle: 'Vue E-Commerce Practice',
                        type: 'Web Application',
                        image: g12
                    },
                    {
                        tittle: 'Website Cek Khodam',
                        type: 'Web / Static',
                        image: g13
                    },
                    {
                       tittle: 'UI Desain Aplikasi',
                        type: 'UI/UX Design',
                        image: g11
                    }
                ]
            }
        }
    }
</script>

<style scoped>
.projects-list{
    display: flex;
    gap: 89px;
    padding: 60px 40px;
    flex-wrap: wrap;
    justify-content: center;
}

.project-card{
    background-color: #F0E4D3;
    overflow: hidden;
    width: 300px;
    position: relative;
    box-shadow: 0 4px 8px rgba(0,0,0,0.05);
    transition: transform 0.3s ease;
}

.project-card:hover{
    transform: translateY(-5px);
}

.project-card img{
    width: 100%;
    height: 160px;
    object-fit: cover;
}

.project-info{
    padding: 15px;
}

.project-info h4{
    margin: 0 0 5px;
    font-size: 16px;
    color: black;
    font-weight: bold;
}

.project-info p{
    font-size: 13px;
    color: black;
}

.arrow-icon{
    position: absolute;
    bottom: 10px;
    right: 10px;
    background: #DCC5B2;
    width: 40px;
    height: 40px;
    border-radius: 999px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 30px;
    color: black;
}

@media (max-width: 768px) {
  .projects-list {
    flex-direction: column;
    gap: 30px;
    padding: 40px 123px;
  }

  .project-card {
    width: 100%;
    max-width: 320px;
  }

  .arrow-icon {
    width: 32px;
    height: 32px;
    font-size: 22px;
    bottom: 8px;
    right: 8px;
  }

  .project-info h4 {
    font-size: 14px;
  }

  .project-info p {
    font-size: 12px;
  }
}

</style>