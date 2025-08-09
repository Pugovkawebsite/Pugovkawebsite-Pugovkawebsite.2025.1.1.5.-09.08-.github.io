<template>
       <div class="hobbies-card" v-for="hobbi in hobbies">
            <img :src="hobbi.img">
            <div class="hobbies-card__text">{{hobbi.name}}</div>
        </div>
            
        

</template>

<script>
export default {
    props: {
        hobbies: {
        type: Array,
        required: true
       } 
    }
}

</script>

<style scoped>
.hobbies-card {
    width: 266px;
    height: 34px;
    display: flex;
    justify-content: space-between;
}
.hobbies-card__text {
    font-weight: 500;
    font-size: 14px;
    color: #47516b;
    width: 215px;
    height: 19px;
    padding-top: 8px;
}

@media(max-width: 767px) { 
    .hobbies-card {
        width: 50%;
    }
    .hobbies-card__text {
        padding-left: 8px;
    }
    .hobbies-card__text {
        display: block;
    }
}

@media(max-width: 459px) {
    .hobbies-card img {
        height: 70%;
        max-width: 37px;
    }
    .hobbies-card__text {
        font-size: 12px;
    }
   
}
</style>