<template>
  <div>
    <h3>{{titol}}</h3>
    <div v-for="(element, index) in llista" :key="index">
      <v-icon>{{ element.icono }}</v-icon>{{ element.text }}
    </div>
  </div>
</template>

<script>
  export default {
    props:['titol', 'llista']
  }
</script>

<style lang="scss" scoped>

</style>