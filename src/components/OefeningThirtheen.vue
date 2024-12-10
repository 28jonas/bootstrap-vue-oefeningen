<template>
  <div class="container mt-5">
    <h2>Progressie Balk</h2>
    <div class="progress mb-3">
      <div class="progress-bar" role="progressbar" :style="{ width: breedte + '%' }">{{ breedte }}%</div>
    </div>
    <button @click="add" class="btn btn-primary">Vergroot</button>
  </div>
</template>
<script>
import {ref} from "vue";

export default{
  setup(){
    let breedte = ref(0)
    const add = () =>{
      if(breedte.value < 100){
        breedte.value = breedte.value +5
      }
    }
    return {breedte, add}
  }
}
</script>