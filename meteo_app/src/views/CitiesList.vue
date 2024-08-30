<script>
import City from "@/components/City.vue";
import {defineComponent} from "vue";

export default defineComponent({
  components: {City},
  data() {
    return {
      name: 'Ma ville', // nom de la ville
      weather: 'Peu nuageux', // descriptif météo
      temperature: 20.55, // température en °C
      updatedAt: new Date().toLocaleString() // date de dernière mise à jour
    }
  },
})

</script>
<template>
  <div class="about">
    <h1>Météo - Liste des villes</h1>
  </div>
  <City :name="name"  :weather="weather" :temperature="temperature" :updatedAt="updatedAt" />/>
</template>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
