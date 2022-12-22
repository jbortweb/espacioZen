<template>
  <div v-if="projecte" style="margin-top:100px; margin-bottom:200px">
    <h2>{{ projecte.titol }}</h2>
    <p class="text-projecte">{{ projecte.text }}</p>
    <div class="container-enlace">
      <a :href="projecte.enlace" target="blank">Visitar proyecto</a>
    </div>
    <v-row style="height:100vh">
      <v-col cols="6" v-for="(imatge, indexImagen) in projecte.imagen" :key="indexImagen">
        <v-img aspect-ratio="2" :src="imatge" class="imagen-proyecto" alt="foto proyecto">
        </v-img>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  props: ["projecte", "numeroSeccion", "numeroProyecto"]
}
</script>

<style lang="scss" scoped>
.imagen-proyecto {
  box-shadow:
    0 -3em 3em rgba(0, 0, 0, 0.1),
    0 0 0 2px rgb(255, 255, 255),
    0.3em 0.3em 1em rgba(0, 0, 0, 0.3);
  margin-top: 20px;
  border-radius: 20px;
}
.container-enlace {
  color:#fff;
}

a {
  text-decoration: none;
  background-color: #000;
  color: #fff !important;
  font-weight: 500;
  padding: 10px;
}
</style>