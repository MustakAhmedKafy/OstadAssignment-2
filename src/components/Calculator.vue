<script setup>
import { ref } from "vue";

const num1 = ref(null);
const num2 = ref(null);
const operator = ref("+");
const result = ref(null);

const calculate = () => {
  if (num1.value !== null && num2.value !== null) {
    switch (operator.value) {
      case "+":
        result.value = num1.value + num2.value;
        break;
      case "-":
        result.value = num1.value - num2.value;
        break;
      case "*":
        result.value = num1.value * num2.value;
        break;
      case "/":
        result.value = num1.value / num2.value;
        break;
      default:
        result.value = null;
    }
  }
};
</script>
<template>
  <div>
    <h2>Calculator</h2>
    <div>
      <input type="number" v-model="num1" placeholder="Enter number 1" />
      <input type="number" v-model="num2" placeholder="Enter number 2" />
      <select v-model="operator">
        <option value="+">+</option>
        <option value="-">-</option>
        <option value="*">*</option>
        <option value="/">/</option>
      </select>
      <button @click="calculate">Calculate</button>
    </div>
    <div v-if="result !== null">
      <p>Result: {{ result }}</p>
    </div>
  </div>
</template>
