<script>
export default {
  /*
    As propriedades retornadas a partir da função "data()" tonam-se estados reativos e deverão ser acessadas através do "this". 
  */
  data() {
    return {
      count: 0,
    };
  },

  /*
    Os métodos são funções que alteram o estado e acionam atualizações. Elas podem ser vinculadas como ouvintes de evento nos templates.
  */
  methods: {
    increment() {
      this.count++;
    },
  },

  /*
    Os métodos de ciclo de vida são chamados em diferentes fases do ciclo de vida do componente. Este método será chamado quando o componente estiver montado. 
  */
  mounted() {
    console.log(`O valor inicial do contador é ${this.count}`);
  },
};
</script>

<template>
  <h3>Count Component Options API</h3>
  <button @click="this.count--">-</button>
  <span>{{ count }}</span>
  <button @click="this.count++">+</button>
</template>

<style scoped>
span {
  margin: 0 20px;
}
</style>
