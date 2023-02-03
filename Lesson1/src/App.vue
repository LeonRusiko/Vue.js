<script>
  import LikeCounter from './components/LikeCounter.vue'
  import RandomNumberGen from './components/RandomNumberGen.vue'
  import MyInfo from './components/MyInfo.vue'
  
  export default{
    components:{
      LikeCounter,RandomNumberGen,MyInfo
    },
  }
</script>

<template>
  <div>
    <MyInfo></MyInfo>
    <LikeCounter></LikeCounter>
    <RandomNumberGen></RandomNumberGen>
  </div>
</template>

<style scoped>

</style>
