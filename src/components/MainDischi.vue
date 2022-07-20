<template>
  <main>
    <CardsList v-for="(poster, index) in posters" :key="poster"
    :poster="index"/>
  </main>
</template>

<script>
import axios from 'axios';
import CardsList from './/CardsList.vue';
export default {
    data:function(){
        return{
            posters : [],
        }
    },
    components:{
        CardsList,
    },
    methods:{
        getMusic(){
           axios.get('https://flynn.boolean.careers/exercises/api/array/music')
           .then((result) =>{
               this.posters = result.data.response;
               console.log(this.posters)
           })
        },
    },
    created(){
            this.getMusic();
        }

}
</script>

<style>

</style>