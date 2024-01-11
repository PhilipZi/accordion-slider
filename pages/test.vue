<template>
  <div>
    <label v-for="i in 4" :key="i" :class="{ active: isChecked[i] }">
      <input type="radio" v-model="isChecked[i]" :value="true" />
      Label {{ i }}
    </label>
  </div>
</template>

<script setup>
import { ref } from "vue";

const isChecked = ref({ 1: true, 2: false, 3: false, 4: false });
</script>

<style scoped>
label {
  display: block;
  margin-bottom: 10px;
  cursor: pointer;
}

.active {
  background-color: lightblue;
}
</style>
