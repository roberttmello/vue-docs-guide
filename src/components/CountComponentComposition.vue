<script setup>
import { ref, onMounted } from "vue";

// O estado reativo
const count = ref(0);

// As funções que alteram o estado e acionam atualizações
function increment() {
  count.value++;
}

function decrement() {
  count.value--;
}

// O método de ciclo de vida
onMounted(() => {
  console.log(`O valor inicial do contador é ${count.value}`);
});
</script>

<template>
  <h3>Count Component Composition API</h3>
  <button @click="decrement">-</button>
  <span>{{ count }}</span>
  <button @click="increment">+</button>
</template>

<style scoped>
span {
  margin: 0 20px;
}
</style>
