<template>
  <h1>meu nome é: {{ nome }}</h1>
  <!--v-bind--->
  <p class="teste">para acessar um link <a v-bind:href="meu_link" target="_blank">Link</a></p>
  <!--v-bind resumido--->
  <img :src='avatar' :alt='descricao'>
</template>
<script>
export default {
  name: "LifeCycle",

  data() {
    return {
      nome: "ainda não sei",
      meu_link:"https://google.com.br",
      avatar:"/public/vite.svg",
      descricao:"vite.svg"
    };
  },

  created() {
    setTimeout(() => {
      this.nome = "Helysson";
      //metodo criado
      this.lifeCycle()
    }, 1000);
  },
  mounted() {
    setTimeout(() => {
      this.nome = "Pedro";
      //metodo criado
      this.lifeCycle()

    }, 2000);
  },
  methods:{
    lifeCycle(){
      console.log("executou lifecycle")
    }
  }
};
</script>
<style>
</style>