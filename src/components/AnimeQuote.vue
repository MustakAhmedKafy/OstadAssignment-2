<script setup>
import { ref } from "vue";

const quoteData = ref(null);

const fetchQuote = async () => {
  try {
    const response = await fetch("https://animechan.xyz/api/random");
    const data = await response.json();
    quoteData.value = data;
  } catch (error) {
    console.error("Error fetching quote:", error);
  }
};
</script>

<template>
  <div>
    <h2>Anime Quote</h2>
    <div v-if="quoteData !== null">
      <p>{{ quoteData.quote }}</p>
      <p>Anime: {{ quoteData.anime }}</p>
      <p>Character: {{ quoteData.character }}</p>
    </div>
    <button class="btn btn-warning" @click="fetchQuote">Get Quote</button>
  </div>
</template>
