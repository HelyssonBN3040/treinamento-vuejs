<template>
  <Header :esta_logado="true"/>
  <h1>Titulo de App Vue!</h1>
  <code>nome: {{ nome }} <br />idade: {{ age }}</code>
  <primeiro-component />
  <LifeCycle/>
  <Pessoa/>
  <Formulario/>
</template>
<script>
import LifeCycle from './components/LifeCycle.vue';
import PrimeiroComponent from "./components/PrimeiroComponent.vue";
import Pessoa from "./components/Pessoa.vue";
import Header from './components/Header.vue';
import Formulario from "./components/Formulario.vue";

export default {
  name: "App",
  components: { PrimeiroComponent, LifeCycle, Pessoa, Header,Formulario },
  data() {
    return {
      nome: "Helysson",
      age: 23,
    };
  },
};
</script>
<style>
/*aplicação de css global*/
  body{
    background-color:#333;
    color: white;

  }
  a{
    color: red;
  }
  .teste{
    background-color: #000;
    
  }
</style>