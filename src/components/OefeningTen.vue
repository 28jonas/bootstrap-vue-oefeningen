<template>
  <div class="container mt-5">
    <h2>Favorieten</h2>
    <input v-model="text" type="text" class="form-control mb-2" placeholder="Voeg een favoriet toe..."/>
    <button @click="toevoegenText" class="btn btn-primary mb-3">Toevoegen</button>
    <ul class="list-group">
      <li class="list-group-item" v-for="(text, index) in favorieten" :key="index" v-text="text"></li>
    </ul>
  </div>
</template>
<script>import {ref} from "vue";

export default {
  setup() {
    const text = ref('');
    const favorieten = ref([]);
    const toevoegenText = () => {
      if (favorieten.value.includes(text.value)) {
        alert("Deze variabele bestaat al")
        text.value = ''
      } else {
        favorieten.value.push(text.value)
        text.value = '';
      }
    }
    return {text, favorieten, toevoegenText}
  }
}</script>
