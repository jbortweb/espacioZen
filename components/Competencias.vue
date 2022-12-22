<template>
  <div>
    <h3>{{titol}}</h3>
    <br>
    <div v-for="element in llista" :key="element.text">
      <v-img class="img-hacemos" :src="element.text"></v-img><br>
    </div>
  </div>
</template>

<script>
  export default {
    props:{
      titol: {
        type:String,
        default:'Sobre mi'
      },
      llista:{
      }
    }    
  }
</script>

<style lang="scss" scoped>

.img-hacemos{
  border-radius: 20px;
}

</style>