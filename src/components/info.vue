<template>
  <p v-if="esta_trabalhando">Estou trabalhando no momento</p>
  <p v-else>Nao estou trabalhando</p>
  <p v-if="1 > 2">teste</p>
  <p>E utilizo as seguintes tecnologias:</p>
  <div>
    <button @click="showEmail">{{ textButton }}</button>
    <p v-show="mostrar_email">mande seu email para: {{ email }}</p>
  </div>
  <!--renderização de lista com v-for e com solução na key mas sem id na lista-->
  <p>Tecnologias FrontEnd</p>
  <ul>
    <li v-for="(technology, index) in Tec_Front" v-bind:key="index">
      {{ technology }}
    </li>
  </ul>
  <!--renderização de lista com v-for e com solução na key-->
  <p>Tecnologias BackEnd</p>
  <ul>
    <li v-for="technology in Tec_Back" :key="technology.id">
      {{ technology.language }}
    </li>
  </ul>
</template>
<script>
export default {
  name: "info",
  data() {
    return {
      esta_trabalhando: false,
      email: "helyssonspt.lnx@gmail.com",
      mostrar_email: false,
      textButton: "Mostrat Email",
      Tec_Front: ["Html", "Css", "React"],
      Tec_Back: [
        { id: 1, language: "Python" },
        { id: 2, language: "JavaScript" },
        { id: 3, language: "PHP" },
      ],
    };
  },
  //criação de metodos
  methods: {
    showEmail() {
      //comando para exibir e esconder o email atraves de click
      this.mostrar_email = !this.mostrar_email;
      //condição para mostrar e esconder texto
      if (!this.mostrar_email) {
        this.textButton = "Mostrar email";
      } else {
        this.textButton = "esconder email";
      }
    },
  },
};
</script>