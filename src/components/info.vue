<template>
  <p v-if="esta_trabalhando">Estou trabalhando no momento</p>
  <p>E utilizo as seguintes tecnologias:</p>
  <ul>
    <li>Javascript</li>
    <li>Python</li>
    <li>C</li>
  </ul>
</template>
<script>
export default {
  name: "info",
  data(){
    return{
      esta_trabalhando:true
    }
  }
};
</script>