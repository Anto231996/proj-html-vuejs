<template>
  <div id="app">
    <HeaderIndex/>
    <MainIndex/>
  </div>
</template>


<script>
import HeaderIndex from './components/HeaderIndex.vue'
import MainIndex from './components/MainIndex.vue'

export default {
  name: 'App',
  components: {
    HeaderIndex,
    MainIndex
  }
}
</script>


<style lang="scss">
@import "./assets/scss/style.scss";
</style>