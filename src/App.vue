<template>
  <div id="app">
   <HeaderDischi />
   <MainDischi />
   <FooterDischi />
  </div>
</template>

<script>
import HeaderDischi from './components/HeaderDischi.vue';
import MainDischi from './components/MainDischi.vue';
import FooterDischi from './components/FooterDischi.vue';



export default {
  name: 'App',
  components: {
    HeaderDischi,
    MainDischi,
    FooterDischi,
    

  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 0;
  padding: 0;
  box-sizing: border-box;

}
body{
  margin: 0;
}
</style>
