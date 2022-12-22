<template>
  <div>
    <v-row style="height: 100vh">
      <v-col class='col-titulo'>
        <span class="esquerra">{{ titolEsquerra }}</span>
        <span class="dreta">{{ titolDreta }}</span>
        <span class="esquerra">.</span>
        <v-row class="fila-linea">
          <v-col md='3' class="linea">
            <hr>
          </v-col>
          <v-col>
            <p class="fecha-linea">{{ subtitol }}</p>
          </v-col>
        </v-row>
        <div class="nom-ofici">
          <v-row>
            <v-col>
              <span class="nom">{{nom}}</span>
            </v-col>
          </v-row>
          <v-row>
            <v-col>
              <span>{{ofici}}</span>
            </v-col>
          </v-row>
        </div>
      </v-col>
    </v-row>

  </div>
</template>

<script>
export default {

  props: [
    'titolEsquerra',
    'titolDreta',
    'subtitol',
    'nom',
    'ofici'
  ],

}


</script>

<style lang="scss" scoped>
.col-titulo {
  padding-top: 40vh;
  height: 10px;
}

.esquerra {
  font-size: 5.1em;
  font-weight: bold;
}

.dreta {
  font-size: 4.3em;
  font-weight: 100;
}
.fila-linea{
  margin-top: -30px;
}
.fecha-linea{
  font-size: 12px;
  margin-top: -8px;
  color: gray;
}

.nom-ofici{
  margin-top: 30vh;
  line-height: 0px;
  color:gray;
  font-size: 18px
}
.nom {
  font-weight: 600;
}

</style>