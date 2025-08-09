<template>
      <div class="description" v-for="user in users">
        <div class="description__persone">
            <img class="description__img" :src="user.img">
            <div class="description__name">{{user.name}}</div>

        </div>
        <div>
          <div class="description__text">{{user.about}}</div>
        <img class="elem__gorizont" src="../img/divider.svg">
          
        </div>
      </div>


            
        

</template>

<script>
export default {
    props: {
        users: {
        type: Array,
        required: true
       } 
    }
}

</script>

<style scoped>
.description__img {
  width: 96px;
  height: 96px;
}
.description__name {
  font-weight: 500;
  font-size: 32px;
  color: #2e2e48;
}
.description__persone {
  width: 266px;
  height: 153px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.description__text {
  font-weight: 500;
  font-size: 16px;
  line-height: 133%;
  color: #47516b;
}
.description {
  height: 340px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
@media(max-width: 987px) {
    .description__name {
        font-size: 26px;
    }
     .elem__gorizont {
        width: 170px;
    }
}
@media(max-width: 767px) {
    .description {
        height: 290px;
    }
    .description__text {
        font-size: 20px;
    }
    .elem__gorizont {
        width: 500px;
        height: 4px;
    }
}
@media(max-width: 575px) {
    .description__text {
        font-size: 16px;
    }
    .elem__gorizont {
        width: 300px;
    }
}
@media(max-width: 459px) {
    .description__text {
        font-size: 15.5px;
    }
    .elem__gorizont {
        width: 260px;
    }
}

</style>
