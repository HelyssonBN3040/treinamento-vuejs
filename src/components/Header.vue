<template>
  <div class="container">
    <nav class="navbar">
      <img :src="avatar" alt="" />
      <ul>
        <li><a href="">Home</a></li>
        <li><a href="">Sobre</a></li>
        <li><a href="">Contato</a></li>
        <li><a href="">Outros</a></li>
      </ul>
    </nav>
  </div>
</template>
<script>
export default {
  name: "Header",
  data() {
    return {
      avatar: "/public/vite.svg",
    };
  },
};
</script>
<!--metodo scoped dentro css aplica estilos somente nesse componente e sem aplica de forma global-->
<style scoped>
ul {
  list-style: none;
  display: flex;
  gap: 1rem;
}
a{
    color: white;
    text-decoration: none;
    transition: 0.3s;
}
a:hover{
    color:rgb(209, 197, 197);
}
.navbar{
    display: flex;
    justify-content: space-around;
    align-items: center;
}
</style>