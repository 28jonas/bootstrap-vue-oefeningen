<template>
  <div class="container mt-5 text-center">
    <h2>Welkom Berichten</h2>
    <h1>Welkom, {{ naam }}</h1>
    <input v-model="naam" type="text" class="form-control mt-3" placeholder="Typ je naam hier..."/></div>
</template>
<script>
import {ref} from "vue";
export default {
  setup() {
    const naam = ref('')
    return {naam}
  }
}</script>
