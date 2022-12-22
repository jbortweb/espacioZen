<template>
  <div class="container-gracias">
    <v-row>
        <v-col cols="12" class="text-gracias">
            <span style="font-weight:900;font-size:40px">{{esquerre}}</span>
            <span style="font-weight:100;font-size:40px">{{dreta}}</span>
        </v-col>
        <v-col cols="12">
            <Contacte
            v-if="contacte"
            class="pt-10"
            :titol="contacte.titol"
            :llista="contacte.llista"
        ></Contacte>
        </v-col>       
    </v-row>
  </div>
</template>
<script>
export default{
    props:["esquerre","dreta","contacte"]
}
</script>
<style lang="scss" scoped>
.container-gracias{
  height: 100vh;
  margin-top: 100px;
}
.text-gracias{
  text-align: center;
}
</style>