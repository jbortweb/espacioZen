<template>
  <div>
    <v-row style=" padding-top: 20vh; padding-left:100px">
      <v-col>
        <v-img 
          :src="imagen"
          alt="Foto personal"
        ></v-img>
      </v-col>
      <v-col class="col-presentacion">
        <span class="presenthola">{{presentHola}}</span>
        <span class="presentsoy">{{presentSoy}}</span>
        <br>
        <span class="present-nom">{{presentNom}}</span>
        <span class="present-ofici">{{presentOfici}}</span>
      </v-col>
    </v-row>

  </div>
</template>

<script>
  export default {
    props: [
      'imagen',
      'presentHola',
      'presentSoy',
      'presentNom',
      'presentOfici',
    ]
  }
</script>

<style lang="scss" scoped>

.col-presentacion{
  padding-top: 200px;
  line-height: 60px;
}
.presenthola{
  font-style: italic;
  font-size: 5rem;
  font-weight: bold;
}
.presentsoy{
  font-size: 5rem;
  font-weight: 200;
  padding-left:10px;
}
.present-nom{
  font-size: 5rem;
  font-weight: bold;
  margin-top: -50px;
}
.present-ofici{
  font-size: 1.5rem;
  color:gray;
  padding-left: 20px;
  margin-top: -50px;
}

</style>