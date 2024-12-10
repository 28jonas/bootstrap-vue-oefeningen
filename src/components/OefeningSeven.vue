<template>
  <div class="container mt-5">
    <h2>Tab Navigatie</h2>
    <ul class="nav nav-tabs">
      <li class="nav-item">
        <a class="nav-link" href="#" :class="{ active: tab.value === 'tab1' }" @click="tab.value='tab1'">Tab 1</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#" :class="{ active: tab.value === 'tab2' }" @click="tab.value='tab2'">Tab 2</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#" :class="{ active: tab.value === 'tab3' }" @click="tab.value='tab3'">Tab 3</a>
      </li>
    </ul>
    <div class="tab-content mt-3">
      <div v-if="tab.value === 'tab1'"><p>Inhoud van Tab 1</p></div>
      <div v-if="tab.value === 'tab2'"><p>Inhoud van Tab 2</p></div>
      <div v-if="tab.value === 'tab3'"><p>Inhoud van Tab 3</p></div>
    </div>
  </div>
</template>
<script>import {ref} from "vue";

export default {
  setup() {
    const tab = ref('tab1'); // Standaard actieve tab
    return {tab};  },};</script>