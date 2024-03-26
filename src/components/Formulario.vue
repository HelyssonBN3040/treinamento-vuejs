<template>
    <form action="" @submit="enviarForm($event)">
        <input type="text" v-model="name">
        <input type="text" v-model="email">
        <input type="submit" value="Enviar">
    </form>    
</template>
<script>
export default{
    name: "Form",
    data(){
        return{
            name: "",
            email: ""
        }
    },
    methods:{
        enviarForm(e){
            e.preventDefault();
            const name = this.name;
            const email = this.email;
            console.log("Formulario Enviado!")
            console.log ("seu nome é: "+ name)
            console.log ("seu email é: "+ email)
        }
    }

}
</script>