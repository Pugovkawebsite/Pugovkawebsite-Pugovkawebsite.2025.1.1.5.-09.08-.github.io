<template>
        <div class="social-card" v-for="social in socials">
            <img class="social-card__img" :src="social.img">
            <div class="social-card__descr">
                <div class="socials__text">{{social.name}}</div>
                <div class="social-card__address">{{social.address}}</div>
            </div>
        </div>
            
        

</template>

<script>
export default {
    props: {
        socials: {
        type: Array,
        required: true
       } 
    }
}

</script>

<style scoped>
.social-card {
    width: 266px;
    height: 40px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}
.social-card__descr {
    width: 217px;
    height: 40px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
}
.social-card__address {
    font-weight: 500;
    font-size: 14px;
    color: #47516b;
}
.social-card__img {
    width: 32px;
    height: 32px;
}

@media(max-width: 767px) {
    .social-card {
        width: 240px;
    }
    .social-card__descr {
        width: 180px;
        height: 50px;
    }
    .social-card__address {
        font-size: 16px;
    }
}
@media(max-width: 575px) {
    
}

@media(max-width: 459px) {
    
}

</style>