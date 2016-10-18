<template>
  <div id="app">
  <top-bar></top-bar>
  <scroll-pic keep-alive></scroll-pic>
  <main-list></main-list>
    <bottom></bottom>
  </div>





</template>

<script>
import TopBar from './components/TopBar.vue'
import ScrollPic from './components/ScrollPic.vue'
  import Bottom from './components/Bottom.vue'
  import MainList from './components/main-list.vue'
  export default {
    components: {
    TopBar,ScrollPic, Bottom,MainList
   }
}
</script>

<style>
  @import '~vux/dist/vux.css';
</style>
