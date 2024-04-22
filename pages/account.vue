 <!--
    Por defecto, todas las páginas utilizan el layout "default".
    Si se quiere utilizar un layout diferente, se debe usar el definePageMeta e indicar el que queremos.
 -->
<script setup>
    definePageMeta({
        layout: "authentication"
    })
</script>

<template>
    <div class="container">
        <div class="row">
            <h1>My account</h1>
        </div>
        <div class="row">
            <div class="6-col">
                <NuxtLink class="btn btn-primary" to="/account">Login</NuxtLink>
                <NuxtLink class="btn btn-primary" to="/account/register">Registrar</NuxtLink>
            </div>
            <div class="6-col">
                <NuxtPage /> <!-- Para renderizar aquí adentro las páginas que están en pages/account/ -->
            </div>
        </div>
    </div>
</template>