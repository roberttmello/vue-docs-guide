<script setup>
import CountComponentOptions from "../src/components/CountComponentOptions.vue";
import CountComponentComposition from "../src/components/CountComponentComposition.vue";
import InterpolationExamples from "./components/InterpolationExamples.vue";
</script>

<template>
  <section class="container">
    <h2>🚩Vue 3 Guia🚩</h2>
    <div class="componentsContainer">
      <CountComponentOptions />
    </div>
    <div class="componentsContainer">
      <CountComponentComposition />
    </div>
    <div class="componentsContainer">
      <InterpolationExamples />
    </div>
  </section>
</template>

<style>
* {
  font-family: monospace;
}
.container {
  max-width: 960px;
  padding: 8px 16px;
  margin: 0 auto;
}
.componentsContainer {
  border: 2px solid #222222;
  padding: 4px 8px;
  margin-top: 8px;
}
</style>
