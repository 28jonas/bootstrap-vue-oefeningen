<template>
  <div class="container mt-5 text-center"><h2>Countdown Timer</h2>
    <p>Tijd: <strong>{{ tijd }}</strong></p>
    <button @click="startTimer" class="btn btn-success">Start</button>
  </div>
</template>
<script>import {ref} from "vue";

export default {
  setup() {
    let tijd = ref(10);
    const startTimer = () => {
      setInterval(() => {
        if (tijd.value >= 0) tijd.value--
      }, 1000)
    }
    return {startTimer, tijd}
  }
}</script>
