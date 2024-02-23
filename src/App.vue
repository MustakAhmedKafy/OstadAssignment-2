<script setup>
import Calculator from "./components/Calculator.vue";
import AnimeQuote from "./components/AnimeQuote.vue";
</script>

<template>
  <div class="main-content container mt-5 pt-5">
   
    <div class="row">
      <div class="col-md-12"> <h1 class="display-4 text-center">Ostad Assignment 2</h1></div>
      <div class="col-md-2 mt-5"></div>
      <div class="col-md-4 mt-5">
        <Calculator />
      </div>
      <div class="col-md-4 mt-5">
        <AnimeQuote />
      </div>
      <div class="col-md-2 mt-5"></div>
    </div>
  </div>
</template>

<style>
.main-content{
  height: 100vh;
  /* vertical-align: middle;
  display: inline-flex;
  align-content: center;
  justify-content: center; */
}
</style>
