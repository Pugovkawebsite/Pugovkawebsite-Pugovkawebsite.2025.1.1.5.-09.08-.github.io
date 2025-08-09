<template>
       <div class="tools-card" v-for="tool in tools">
            <div class="tools-card__wrap">
            <div><img :src="tool.img"></div>
                <div class="tools-card__text">
                    <div class="tools-card__name">{{tool.name}}</div>
                    <div class="tools-card__function">{{tool.function}}</div>
                </div>

            </div>
        </div>
            
        

</template>

<script>
export default {
    props: {
        tools: {
        type: Array,
        required: true
       } 
    }
}

</script>

<style scoped>
.tools-card {
    border-radius: 0 0 0 8px;
    width: 133px;
    height: 112px;
    background: #f7f9fc;
    display: flex;
    justify-content: center;
    align-items: center;
}
.tools-card__text {
    margin-top: 8.07px;
}
.tools-card__wrap {
    display: flex;
    flex-direction: column;
    align-items: center;

}
.tools-card__text {
    height: 34px;
}
.tools-card__name {
    font-weight: 500;
    font-size: 14px;
    color: #2e2e48;
    text-align: center;
}
.tools-card__function {
    font-weight: 400;
    font-size: 10px;
    color: #79819a;
    text-align: center;
}
@media(max-width: 1199px) {
    .tools-card {
        width: 111px;
    }
}
@media(max-width: 987px) {
    .tools-card {
        width: 101px;
    }
}
@media(max-width: 575px) {
    .tools-card__wrap {
        flex-direction: row;
    }
    .tools-card {
        width: 135px;
        height: 90px;
    }
}
@media(max-width: 459px) {
    .tools-card__wrap div img {
        height: 70%;
        max-width: 70%;
    }
    .tools-card {
        width: 125px;
        height: 82px;
        padding-left: 2px; 
        padding-right: 6px;
    }
    .tools-card__wrap {
        justify-content: start;
    }
    
}

</style>