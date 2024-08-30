<script>
export default {

  props : ['name', 'weather', 'temperature', 'updatedAt']
}
</script>

<template>
  <h2>{{name}}</h2>

  <p> La météo du jour est {{weather}}.</p>
  <p> La température actuelle est de {{temperature}}°C.</p>
  <p> Mis à jour le {{updatedAt}}.</p>
</template>

<style scoped>

</style>