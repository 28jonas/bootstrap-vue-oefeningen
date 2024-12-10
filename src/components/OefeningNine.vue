<template>
  <div class="container mt-5 text-center">
    <h2>Dynamische Tekstkleur</h2>
    <input type="color" class="form-control mt-3" v-model="kleur"/>
    <p class="mt-3" :style="{color:kleur}">Dit is een voorbeeldtekst.</p></div>
</template>
<script>import {ref} from "vue";

export default {
  setup() {
    const kleur = ref('#101010');
    return {kleur}
  }
}</script>
