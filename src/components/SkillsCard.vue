<template>
       <div class="skills-card" v-for="skill in skills">
            
            <img :src="skill.img">
            <div class="skills-card__wraper">
                <div class="skills-card__name"> {{skill.name}} </div>
                <div class="skills-card__function"> {{skill.function}} </div>
            </div>
        </div>
            
        

</template>

<script>
export default {
    props: {
        skills: {
        type: Array,
        required: true
       } 
    }
}

</script>

<style scoped>
.skills-card {
    border-radius: 8px 0 0 0;
    padding: 16px;
    width: 227px;
    height: 129px;
    background: #f7f9fc;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
}
.skills-card__name {
    font-weight: 500;
    font-size: 14px;
    color: #2e2e48;
    text-align: center;
}
.skills-card__function {
    font-weight: 400;
    font-size: 10px;
    text-align: center;
    color: #79819a;
}
@media(max-width: 1199px) {
    .skills-card {
        width: 190px;
    }
}
@media(max-width: 987px) {
    .skills-card {
        width: 175px;
    }
}

@media(max-width: 767px) {
    .skills-card {
        width: 166px;
        padding: 4px;
    }  
    .skills-card__name {
        font-size: 16px;
        margin-bottom: 8px;
    }
    .skills-card__function {
        font-size: 12px;
    }
    .tools-card {
        width: 98px;
        height: 130px;
    }
    .tools-card__function {
        font-size: 12px;
    }
}
@media(max-width: 575px) {
    .skills-card {
        border-radius: 8px 0 0 0;
        padding: 16px;
        width: 227px;
        height: 83px;
        flex-direction: row;
    }
}


</style>