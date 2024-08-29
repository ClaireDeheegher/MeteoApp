<script>
export default {
  data() {
    return {
      name: 'Ma ville', // nom de la ville
      weather: 'Peu nuageux', // descriptif météo
      temperature: 20.55, // température en °C
      updatedAt: new Date() // date de dernière mise à jour
    }
  }
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