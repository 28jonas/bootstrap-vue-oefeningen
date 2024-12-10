<template>
  <div class="container mt-5 text-center"><h2>Simpele Rekenmachine</h2>
    <input v-model="getal1" type="number" class="form-control mb-2" placeholder="Getal 1"/> <input
      v-model="getal2" type="number" class="form-control mb-2" placeholder="Getal 2"/>
    <button @click="optellen" class="btn btn-primary mb-3">Optellen</button>
    <h3>Resultaat: {{ som }}</h3></div>
</template>
<script>import {ref} from "vue";

export default {
  setup() {
    const getal1 = ref(0)
    const getal2 = ref(0)
    let som = ref(0)
    const optellen = () => {
      som.value = getal1.value + getal2.value
    }
    return {getal1, getal2, optellen, som}
  }
}</script>
