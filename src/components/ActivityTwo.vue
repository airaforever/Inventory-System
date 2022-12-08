<script setup>
import { ref } from "vue";
let number = ref(0);
let number2 = ref(0);

let result = ref(0);

function add() {
  result.value = parseInt(number.value) + parseInt(number2.value);
}

function subtract() {
  result.value = parseInt(number.value) - parseInt(number2.value);
}
</script>

<template>
  <div>Calculator</div>
  <input type="text" v-model="number" />
  <input type="text" v-model="number2" />

  <div>
    <button @click="add">+</button>
    <button @click="subtract">-</button>
  </div>

  <div>Total: {{ result }}</div>
</template>

<style>
.number {
  color: rgb(220, 8, 209);
  font-size: 50px;
  font-weight: bold;
  margin-bottom: 20px;
  text-align: center;
  padding: 10px;
  background-color: rgb(10, 232, 198);
}
.wrapper {
  display: flex;
  grid-gap: 40px;
}
</style>
