<template>
  <div>
    <v-row>
      <v-col>
        <div v-for="(element,indexLista) in lista" :key="indexLista">
          <p class="indice-proyectos">0{{ indexLista+1 }}</p>
          <p class="titulo-proyecto">{{ element.titol }}</p>
          <div v-for="(projecte, indexProjecte) in element.projectes" :key="indexProjecte">
            <Proyectos
              :projecte= "projecte"
              :numeroSeccion = "indexLista"
              :numeroProyecto= "indexProjecte"
            >
            </Proyectos>
          </div>
        </div>
      </v-col>
    </v-row>
  </div>
</template>

<script>
import Proyectos from './Proyectos.vue'
  export default {
  components: { Proyectos },
    props:['lista']
  }
</script>

<style lang="scss" scoped>
.indice-proyectos{
  font-size: 8rem;
  font-weight: 100;
  margin-bottom: -30px;
}
.titulo-proyecto{
  font-size: 2rem;
  font-weight: 500;
}

</style>