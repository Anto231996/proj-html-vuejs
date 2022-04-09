<template>
  <div id="app">
    <HeaderIndex/>
    <MainIndex/>
    <FooterIndex/>
  </div>
</template>


<script>
import HeaderIndex from './components/HeaderIndex.vue'
import MainIndex from './components/MainIndex.vue'
import FooterIndex from './components/FooterIndex.vue'

export default {
  name: 'App',
  components: {
    HeaderIndex,
    MainIndex,
    FooterIndex
  }
}
</script>


<style lang="scss">
@import "./assets/scss/style.scss";
@import url('https://fonts.googleapis.com/css2?family=Hurricane&family=Nunito:ital,wght@0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

div#app{
  font-family: 'Nunito', sans-serif;
}
</style>