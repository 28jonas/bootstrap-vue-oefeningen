<template>
  <div class="container mt-5">
    <h2>Zoekfunctie</h2>
    <input type="text" class="form-control mb-3" placeholder="Zoek eennaam..." v-model="naamZoeken"/>
    <ul class="list-group">
      <li class="list-group-item" v-for="(naam, index) in gefilterdeNamen" :key="index">{{ naam }}</li>
    </ul>
  </div>
</template>
<script>
import {ref, computed} from "vue";

export default{
  setup(){
    const naamZoeken = ref('')
    const namen= ref(['Jonas', 'Tom', 'Kato', 'Laurein'])
    const gefilterdeNamen = computed(() =>
        namen.value.filter((naam) =>
            naam.toLowerCase().includes(naamZoeken.value.toLowerCase())
        )
    );

  return{naamZoeken,gefilterdeNamen, namen}
  }
}
</script>