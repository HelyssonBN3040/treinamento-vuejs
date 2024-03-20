<template>
  <h1>meu nome é: {{ nome }}</h1>
  <p>para acessar um link <a v-bind:href="meu_link" target="_blank">Link</a></p>
</template>
<script>
export default {
  name: "LifeCycle",

  data() {
    return {
      nome: "ainda não sei",
      meu_link:"https://google.com.br"
    };
  },

  created() {
    setTimeout(() => {
      this.nome = "Helysson";
    }, 1000);
  },
  mounted() {
    setTimeout(() => {
      this.nome = "Pedro";
    }, 2000);
  },
};
</script>
<style>
</style>