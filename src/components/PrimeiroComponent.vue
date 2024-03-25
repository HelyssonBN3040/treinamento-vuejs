<template>
    <h3>Titulo vindo do componente!</h3>
    <code>nome {{ nome }}, gerado dentro de uma lista do componente!</code>
    <!--TRabalhando com multiplos eventos-->
    <button @click="primeiro(txt1,$event), segundo(txt2, $event), terceiro()">Ativar multiplos eventos</button>
    <p>{{ multiplos_eventos }}</p>
</template>
<script>
    export default {
        name: "PrimeiroComponent",
        data(){
            return{
                nome:"Luiz",
                multiplos_eventos:'',
                txt1:"Primeiro evento",
                txt2: "Segundo evento"

            }
        },
        methods:{
            primeiro(txt1, e){
                this.multiplos_eventos= txt1
            },
            segundo(txt2,e){
                setTimeout(()=>{
                    this.multiplos_eventos=txt2
                }, 1500)
            },
            terceiro(){
                setTimeout(()=>{
                    this.multiplos_eventos=""
                }, 2500)
            }
        }
    }
</script>