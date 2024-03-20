<template>
  <div>
    <h2>Este é um nome de uma pessoa: {{ nome }}</h2>
  </div>
</template>
<script>

export default {
  name: "Pessoa",
  data() {
    return {
      nome: "Helysson",
    };
  },
};

</script>