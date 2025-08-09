<template>
       <div class="contact-card" v-for="contact in contacts">
            <div class="contact-card__img">
                <img :src="contact.img">
            </div>
           <div class="contact-card__text">
            <div class="contact-card__name">{{contact.name}}</div>
            <div class="contact-card__address">{{contact.address}}</div>
           </div>
        </div>
            
        

</template>

<script>
export default {
    props: {
        contacts: {
        type: Array,
        required: true
       } 
    }
}

</script>

<style scoped>
.contact-card {
    width: 266px;
    height: 40px;
    display: flex;
    justify-content: space-between;
}
.contact-card__img {
    border-radius: 202px;
    width: 32px;
    height: 32px;
    background: #e2e6ee;
    display: flex;
    justify-content: center;
    align-items: center;
}
.contact-card__text {
    width: 217px;
    height: 40px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
}
.contact-card__name {
    font-weight: 400;
    font-size: 12px;
    color: #79819a;
}
.contact-card__address{
    font-weight: 500;
    font-size: 14px;
    color: #47516b;
}
@media(max-width: 1199px) {
    .contact-card__address {
        word-break: break-all;
    }
}

@media(max-width: 987px) {
    .contact-card__address {
        word-break: break-all;
    }
    .contact__wrap {
        width: 170px;
    }
  .contact-card {
        width: 170px;
    }
  .contact-card__address {
        font-size: 11px;
    }
  .contact-card__text {
        width: 118px;
    }

}
@media(max-width: 767px) {
    .contact-card__address {
        font-size: 16px;
    }
    .contact-card {
        width: 350px;
    }
    .contact-card__text {
        width: 320px;
    }
    .contact-card__name {
        font-size: 16px;
    }
}
@media(max-width: 575px) {
    .contact-card__address {
        font-size: 14px;
    }
}
@media(max-width: 459px) {
    .contact-card__name {
        font-size: 15px;
    }
    .contact-card__img img {
        width: 60%;
        height: 60%;
    }
    .contact-card__img {
        width: 25px;
        height: 25px;
        margin-top: 10px;
    }
    .contact-card__address {
        overflow: hidden;
        text-overflow: ellipsis;
        white-space: nowrap;
    }
    .contact-card__text {
        width: 230px;
    }
    .contact-card {
        width: 270px;
    }
}
</style>