<template>
    <div class = "box">
        <div class="imgTeams">
            <img :src="member.imagen" alt="imagenes del equipo" height="200" width="200">
        </div>
        <div class="integrante">
            <h3> <b>{{member.rol}}</b> </h3>
            <h3> {{member.codigo}} {{member.nombre}} </h3>
            <p>{{member.descripcion}}</p>
        </div>
    </div>
</template>

<script>
    export default {
        name: "TeamCard",
        props: ['member']
    }
</script>

<style scoped>

</style>
