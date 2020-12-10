<template>
  <div class="informer-container">
    <temperature></temperature>

    <div class="flex-break"></div>

    <Wet></Wet>

    <div class="vertical-divider"></div>

    <wind></wind>

  </div>
</template>

<script>
import Wet from './Wet.vue'
import Wind from './Wind.vue'
import Temperature from './Temperature.vue'

export default {
  name: "Wrapper",
  data(){
    return {text: 'Я новый компонент!'}
  },
  components:{
    Wet, Wind, Temperature
  }
}
</script>

<style>
.informer-container {
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  flex-wrap: wrap;
  width: 400px;
  min-height: 255px;
  padding: 30px;
  background-image: url('~@/assets/forest.png');
  background-size: cover;
  background-position: center center;
  border-radius: 20px;
  box-shadow: 0px 0px 10px 0px rgba(50, 50, 50, 0.75);
}

.flex-break{
  flex-basis: 100%;
  height: 0;
}

.vertical-divider{
  height: 70px;
  width: 1px;
  background-color: #fff;
  vertical-align: middle;
  display: table-cell;
}
</style>