<template>
       <div class="certificates-card" v-for="certificate in certificates">
            <img :src="certificate.img">
            <div class="certificates-card__text">
                <div class="certificates-card__company">{{certificate.company}}</div>
                <div class="certificates-card__name">{{certificate.name}}</div>

            </div>
            <div class="certificates-card__time">{{certificate.time}}</div>
        </div>
            
        

</template>

<script>
export default {
    props: {
       certificates: {
        type: Array,
        required: true
       } 
    }
}

</script>

<style scoped>
.certificates-card {
    border-radius: 8px 8px 0 0;
    padding: 15px 23px;
    width: 641px;
    height: 74px;
    background: #f7f9fc;
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
}
.certificates-card__text {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    width: 412px;
}
.certificates-card__company {
    font-weight: 400;
    font-size: 13px;
    letter-spacing: 0.01em;
    color: #79819a;
}
.certificates-card__name {
    font-weight: 500;
    font-size: 15px;
    color: #2e2e48;
}
.certificates-card__time {
    font-weight: 400;
    font-size: 11px;
    color: #47516b;
}
@media(max-width: 1199px) {
    .certificates-card {
        width: 588px;
    }
    .certificates-card__text {
        width: 400px;
    }
}
@media(max-width: 987px) {
    .certificates-card {
        width: 532px;
    }
    .certificates-card__text {
        width: 300px;
    }
}
@media(max-width: 767px) {
    .certificates-card {
        width: 503px;
    }
    .certificates-card__text {
        width: 290px;
    }
    .certificates-card__time {
        font-size: 12px;
    }
    
}
@media(max-width: 575px) {
    .certificates-card {
        padding: 15px 6px;
        width: 300px;
        
    }
    .certificates-card__text {
        margin-left: 9px;
    }
    .certificates-card__name {
        font-size: 14px;
    }
}
@media(max-width: 459px) {
    .certificates-card img {
        width: 30px;
        
    }
    .certificates-card {
        width: 250px;
    }
    .certificates-card__text {
        width: 120px;
    }
    .certificates-card__name {
        font-size: 12px;
    }
    .certificates-card__time {
        font-size: 11px;
    }
    .certificates-card__time {
        max-width: 60px;
    }
}
</style>