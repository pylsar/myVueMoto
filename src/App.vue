<template>
  <div id="app">
    <the-header />
    <the-content/>
  </div>
</template>
<script>
import TheHeader from '@/components/TheHeader.vue'; 
import TheContent from './components/TheContent.vue';
export default{
  components:{
    TheHeader,
    TheContent
  }
}
</script>

<style lang="scss">
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
#app{
  width: 100%;
  height: 100vh;
  background-image: url('./assets/img/bg.png');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

</style>
