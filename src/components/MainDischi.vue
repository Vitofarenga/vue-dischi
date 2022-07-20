<template>
  <main>
    <CardsList v-for="(poster, index) in posters" :key="index"
    :poster="poster"/>
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
main{
    background-color: rgba(30,45,59,255);
    display: flex;
    flex-wrap: wrap;
    
}

</style>