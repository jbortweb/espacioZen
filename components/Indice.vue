<template>
  <div>
    <v-row style="height:100vh;">
      <v-col>
        <div class="container-indice">
          <h2  
            v-for='(element ,index) in trabajo' 
            :key="index"
          >
            {{ element.titol }} <span>0{{index +1}}</span>
          </h2>
        </div>

      </v-col>
    </v-row>

  </div>
</template>

<script>
  export default {
    props:['trabajo']
  }
</script>

<style lang="scss" scoped>

  .container-indice{
    padding-left: 100px;
    padding-top: 20vh;
    font-size: 20px;
  }

  .container-indice h2{
    width: 100%;
    margin-bottom: 10px;
    font-weight: 500;
  }

  .container-indice span{
    font-size: 34px;
    font-weight: 200;
  }
</style>