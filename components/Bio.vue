<template>
  <div>
    <v-row style=" padding-top:100px; margin-bottom:100px">
      <v-col>
      <h1 cols='12' md="8" class="sobreMi">{{informacio.titol}}</h1>
      <p class="descripcio">{{informacio.descripcio}}</p>
      </v-col>
      <v-col cols="'12" md="4" v-if="informacio" class="col-competencias">
        <Competencias 
          :titol="informacio.c1.titol" 
          :llista="informacio.c1.llista">
        </Competencias>
          <br><br>
        <div class="contact">
          <Contacte
            :titol="informacio.informacioContacte.titol"
            :llista="informacio.informacioContacte.llista"></Contacte>
        </div>
      </v-col>
    </v-row>
  </div>
</template>

<script>
import Competencias from './Competencias.vue';
import Contacte from './Contacte.vue';

export default {
  components: { Competencias, Contacte },
  props:['informacio']

}

</script>

<style lang="scss" scoped>
.sobreMi {
  font-size: 2rem;
  font-weight: bold;
  line-height: 50px;
  white-space: pre-wrap;
  white-space: -moz-pre-wrap;
  white-space: -o-pre-wrap;
  line-height: 30px;
  margin-bottom: 20px;
}

.descripcio {
  padding-left: 100px;
  width: 85%;
  white-space: pre-wrap;
  white-space: -moz-pre-wrap;
  white-space: -o-pre-wrap;
}
.contact h3{
  padding-bottom: 10px;
}
.contact p{
  line-height: 8px;
}
.col-competencias{
  padding-left: 70px;
}
</style>