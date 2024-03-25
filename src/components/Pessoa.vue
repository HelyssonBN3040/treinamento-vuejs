<template>
  <div>
    <h2>Este é um nome de uma pessoa: {{ nome }}</h2>
    <Info/>
  </div>
</template>
<script>
import Info from './info.vue';

const lista = ["helysson", "Adriano", "Mabyle"];
console.log(lista)
export default {
  components:{Info},
  name: "Pessoa",
  data() {
    return {
      nome: "Helysson",
    };
    
  },
};

</script>