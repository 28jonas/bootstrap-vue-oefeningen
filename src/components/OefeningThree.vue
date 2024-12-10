<template>
  <div class="container mt-5 text-center"><h2>Lichtschakelaar</h2>
    <p>Licht is: <strong>{{ lichtStatus ? 'aan' : 'uit' }}</strong></p>
    <button @click="toggleLicht" class="btn btn-primary">Schakel</button>
  </div>
</template>
<script>import {ref} from "vue";

export default {
  setup() {
    const lichtStatus = ref('aan')
    const toggleLicht = () => {
      lichtStatus.value = !lichtStatus.value;
    }
    return {lichtStatus, toggleLicht}
  }
}</script>
