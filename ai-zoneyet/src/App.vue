<template>
  <div id="app">
    <app-header></app-header>
    <div style="margin: 0 auto;width: 1200px;border: solid 1px #666666">
      <router-view/>
    </div>
  </div>
</template>

<script>
import AppHeader from '@/components/header_com/header_index';


export default {
  name: 'App',
  data(){
    return{

    }
  },

  components:{
    AppHeader
  },
  mounted(){

  }



}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  width: 100%;
}
</style>
