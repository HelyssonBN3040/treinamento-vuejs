<template>
  <h1>Titulo de App Vue!</h1>
  <code>nome: {{ nome }} <br />idade: {{ age }}</code>
  <primeiro-component />
  <LifeCycle/>
  <Pessoa/>
</template>
<script>
import LifeCycle from './components/LifeCycle.vue';
import PrimeiroComponent from "./components/PrimeiroComponent.vue";
import Pessoa from "./components/Pessoa.vue";


export default {
  name: "App",
  components: { PrimeiroComponent, LifeCycle, Pessoa },
  data() {
    return {
      nome: "Helysson",
      age: 23,
    };
  },
};
</script>