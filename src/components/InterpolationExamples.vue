<script setup>
import { ref } from "vue";
const msg = ref("My message");
const rawHtml = ref("My text");
const dynamicId = ref("myId");
</script>

<template>
  <h3>Interpolation Examples</h3>
  <span><strong>Message</strong>: {{ msg }}</span>
  <br />
  <br />
  ---
  <p>Using text interpolation: {{ rawHtml }}</p>
  <p>Using v-html directive: <span v-html="rawHtml"></span></p>
  <br />
  ---
  <p v-bind:id="dynamicId">
    Dynamic IDs with <strong>v-bind:id="dynamicId"</strong>
  </p>
  <p :id="dynamicId">
    Dynamic IDs with shorthand <strong>:id="dynamicId"</strong>
  </p>
  <br />

  <!-- o mesmo que `:id="id"` -->
  <div :id="something">
    {{ `
    <div :id></div>
    ` }}
  </div>
  <h4>o mesmo que `:id="id"`</h4>
  <br />
  <!-- isto também funciona -->
  <div v-bind:id="something">
    {{`
    <div v-bind:id></div>
    `}}
  </div>
  <h4>isto também funciona</h4>
</template>

<style scoped></style>
