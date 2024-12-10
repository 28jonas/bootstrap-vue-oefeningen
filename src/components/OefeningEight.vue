<template>
  <div class="container mt-5 text-center"><h2>Teller</h2>
    <h1>{{ waarde }}</h1>
    <button @click="waarde++" class="btn btn-success me-2">+</button>
    <button @click="waarde--" class="btn btn-danger me-2">-</button>
    <button @click="waarde=0" class="btn btn-secondary">Reset</button>
  </div>
</template>
<script>import {ref} from "vue";

export default {
  setup() {
    const waarde = ref(0);
    return {waarde}
  }
}</script>
