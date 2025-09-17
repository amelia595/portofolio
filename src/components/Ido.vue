<template>
<section class="things-section">
    <div class="things-left">
        <div class="thing-row" v-for="(item, index) in skills" :key="index">
            <div class="number">{{ index + 1 < 10 ? `0${index + 1}` : index + 1 }}</div>
            <div class="content">
                <h4>{{ item.title }}</h4>
                <hr/>
                <ul>
                    <li v-for="(sub, i) in item.subskills" :key="i">
                        ✅ {{ sub }}
                    </li>
                </ul>
            </div>
            <div class="arrow">↗</div>
        </div>
    </div>

    <div class="things-right">
        <h3>Things I <span class="can-do">Can</span> Do</h3>
        <p style="color:black;">Beberapa hal yang bisa saya kerjakan mulai dari desain UI/UX hingga membuat tampilan web yang interaktif</p>
    </div>
</section>
</template>

<script>
export default {
    name: 'ThingsIDo',
    data(){
        return{
            skills: [
                {
                    title: 'UI/UX Design',
                    subskills: ['Web Design', 'App UI']
                },
                {
                    title: 'Frontend',
                    subskills: ['HTML, CSS', 'JavaScript', 'Vue.js']
                },
                {
                    title: 'Backend',
                    subskills: ['Laravel', 'CRUD']
                }
            ]
        }
    }
}
</script>

<style scoped>
.ThingsIDo{
    color:black;
}
.things-section {
    display: flex;
    justify-content: space-between;
    padding: 60px 40px;
    background-color: #F0E4D3;
    flex-wrap: wrap;
    gap: 40px;
}

.things-left{
    flex: 1;
    max-width: 600px;
}

.thing-row{
    display: flex;
    align-items: flex-start;
    margin-bottom: 30px;
}

.number{
    font-size: 20px;
    width: 40px;
    color: black;
    margin-left: 50px;
}

.content{
    flex: 1;
}

.content h4{
    margin: 0;
    font-size: 18px;
    font-weight: bold;
    color: black;
}

.content hr{
    border: none;
    border-top: 1px solid #918E8E;
    margin: 8px 0;
    width: 98%;
    color:black;
}

.content ul{
    list-style: none;
    padding: 0;
    display: flex;
    flex-wrap: wrap;
    gap: 10px 20px;
    font-size: 13px;
    color:black;
}

.arrow{
    font-size: 30px;
    margin-left: 10px;
    color: black;
    background-color: #DCC5B2;
    width: 35px;
    height: -50px;
    bottom: 30px;
    right: 30%;
    border-radius: 999px;
    align-items: center;
    justify-content: center;
    padding: 5px;
    margin-bottom: 10px;
}

.things-right{
    max-width: 400px;

}

.things-right h3{
    font-size: 24px;
    margin-top: 30px;
    margin-bottom: 10px;
    font-weight: bold;
    color: black;
}

.can-do{
    color: #D9A299;
    font-family: 'Oleo Script Swash Caps', cursive;
}

.things-right p{
    font-size: 14px;
    color: black;
    margin-bottom: 20px;
    margin-right: 60px;
}



</style>