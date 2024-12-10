<template>
  <div class="container mt-5">
    <h2>Mijn Lijst</h2>
    <input v-model="item" type="text" class="form-control mb-2" placeholder="Voeg een item toe..."/>
    <button @click="voegToe" class="btn btn-success mb-3">Toevoegen</button>
    <ul class="list-group">
      <li class="list-group-item" v-for="(item, index) in items" :key="index" v-text="item"></li>
    </ul>
  </div>
</template>
<script>import {ref} from "vue";

export default {
  setup() {
    const items = ref([]);
    const item = ref('')
    const voegToe = () => {
      items.value.push(item.value);
      item.value = ''
    }
    return {item, items, voegToe}
  }
}</script>
