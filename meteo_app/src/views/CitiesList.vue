<script>
import City from "@/components/City.vue";
import {defineComponent} from "vue";
import relativeTime from "dayjs/plugin/relativeTime";
import dayjs from "dayjs";
dayjs.extend(relativeTime);


export default defineComponent({
  components: {City},
  data() {
    return {

      cities: [
        {
          id: 1,
          name: 'Ville 1',
          weather: 'Ensoleillé',
          temperature: 22.0,
          updatedAt: dayjs(new Date()).toNow()
        },
        {
          id: 2,
          name: 'Ville 2',
          weather: 'Peu nuageux',
          temperature: 19.5,
          updatedAt: dayjs(new Date()).toNow()
        }
      ]
    }

  },
})

</script>
<template>
  <div class="about">
    <h1>Météo - Liste des villes</h1>
  </div>
  <City v-for="city in cities" :key="city.id" :name="city.name" :weather="city.weather" :temperature="city.temperature" :updatedAt="city.updatedAt" />
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
