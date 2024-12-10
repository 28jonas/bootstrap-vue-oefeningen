<template>
  <div class="container mt-5">
    <h2>Cirkel Tekenaar</h2>
    <label for="radiusInput">Straal:</label>
    <input type="number" id="radiusInput" class="form-control" placeholder="Straal in pixels" v-model="straal" />
    <div class="mt-3" style="background-color: lightblue; border-radius:50%;" :style="{width: straal + 'px', height: straal + 'px'}"><br></div>
  </div>
</template>
<script>
import {ref} from "vue";

export default {
  setup(){
    const straal = ref(25)
    return{straal}
  }
}
</script>
