<template>
    <h3>Titulo vindo do componente!</h3>
    <code>nome {{ nome }}, gerado dentro de uma lista do componente!</code>
</template>
<script>
    export default {
        data(){
            return{
                nome:"Luiz",

            }
        }
    }
</script>