<template>
    <div>
        <button @click="$emit('mudarImagem')">Trocar Imagem de perfil</button>
    </div>
</template>
<script>
export default {
    name:"MudarImagem",
    emits:["mudarImagem"]
    
}
</script>