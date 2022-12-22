<template>
  <div>
    <Inici
      v-if="portfoliVue"
      :titolEsquerra="portfoliVue.inici.titolEsquerra"
      :titolDreta="portfoliVue.inici.titolDreta" 
      :subtitol="portfoliVue.inici.subtitol"
      :nom="portfoliVue.inici.nom"
      :ofici="portfoliVue.inici.ofici"
    >
    </Inici>
    <Hola
      v-if="portfoliVue"
      :imagen="portfoliVue.hola.imagen"
      :presentHola="portfoliVue.hola.presentHola"
      :presentSoy="portfoliVue.hola.presentSoy"
      :presentNom="portfoliVue.hola.presentNom"
      :presentOfici="portfoliVue.hola.presentOfici"
    >
    </Hola>
    <Bio
    v-if="portfoliVue"
    :informacio="portfoliVue.bio"
    >
    </Bio>
    <Indice
    v-if="portfoliVue"
    :trabajo="portfoliVue.index.llista"
    >
    </Indice>
    <Lista-proyectos
    v-if="portfoliVue"
    :lista="portfoliVue.index.llista"
    >
    </Lista-proyectos>
    <Gracias
    v-if="portfoliVue"
    :esquerre="portfoliVue.gracias.esquerra"
    :dreta="portfoliVue.gracias.dreta"
    :contacte="portfoliVue.bio.informacioContacte"
    >
    </Gracias>
  </div>
</template>

<script>
  
  import portfoli from "@/dades/portfoli"
  import Inici from '../components/Inici.vue';
  import Hola from '../components/Hola.vue';
import Contacte from "../components/Contacte.vue";
import Indice from '../components/Indice.vue';
import ListaProyectos from '../components/ListaProyectos.vue';
import Gracias from '../components/Gracias.vue';
import '../layouts/global.css';



  export default {
    components: { Inici, Hola, Contacte, Indice, ListaProyectos, Gracias, Gracias },
    mounted(){
      this.portfoliVue = portfoli;
    },
    data() {
      return{
      portfoliVue: null
      }
    }

  }
</script>

<style lang="scss" scoped>
*{
  font-family: Montserrat;
}

</style>