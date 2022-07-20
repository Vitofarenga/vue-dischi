<template>
  
    <div>
    <img :src="poster.poster" alt="">
    <p class="p1">{{poster.title}}</p>
    <p>{{poster.author}}</p>
    <p>{{poster.genre}} <br>{{poster.year}}</p>
    </div>
  
</template>

<script>
export default {
    props:['poster'],
}
</script>

<style scoped>
img{
width: 10rem;
height: 10rem;
}
.p1{
color: white;
font-weight:bold ;
}
p{
  color: rgba(100,106,112,255);
}
div{
  margin-left: 7rem;
  padding: 2rem;
  background-color: rgba(46,58,70,255);
  margin-top:2rem ;
  
}
#container{
  display: flex;

}

</style>