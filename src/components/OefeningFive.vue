<template>
  <div class="container mt-5 text-center">
    <h2>Dynamische Achtergrond</h2>
    <input type="color" class="form-control mt-3" v-model="color"/>
    <div class="mt-3 p-5 text-black" :style="{backgroundColor: color}">Dit is een voorbeeldvak</div>
  </div>
</template>
<script>import {ref} from "vue";

export default {
  setup() {
    const color = ref('#fff');
    return {color}
  }
}</script>
