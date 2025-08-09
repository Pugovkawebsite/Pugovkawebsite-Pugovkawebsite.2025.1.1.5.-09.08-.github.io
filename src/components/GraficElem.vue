<template>
    <div class="elem">
      <div class="elem__ball__wrap">
          <img src="../img/graffic/1.svg">
      </div>
        <div class="elem__line__wrap">
            <div class="elem__line"></div>
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
.elem__line {
  border: 2.02px solid #e2e6ee;
  width: 0.5px;
  height: 100%;
}
.elem {
  width: 96.81px;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
}
.elem__ball__wrap {
  width: 32px;
  height: 32px;
  border-radius: 202px;
  box-shadow: inset 0 2px 2px 0 rgba(0, 0, 0, 0.04), 0 12px 48px 0 rgba(0, 0, 0, 0.04), 0 2px 8px 0 rgba(0, 0, 0, 0.05);
  background: #fff;
  display: flex;
  justify-content: center;
  align-items: center;
}
.elem__line__wrap {
  width: 32.27px;
  display: flex;
  justify-content: center;
  height: 100%;
}
@media(max-width: 1199px) {
  .elem {
    width: 86.81px;
  }
}
@media(max-width: 987px) {
  .elem {
    width: 70.81px;
  }
}
@media(max-width: 767px) {
  .elem {
    width: 66.81px;
  }
}
@media(max-width: 575px) {
  .elem {
    width: 36.81px;
  }
}
</style>