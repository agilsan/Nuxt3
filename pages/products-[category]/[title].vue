<script setup>
    const route = useRoute();

    // para validaciones sencillas, sin usar middleware, podemos hacer esto
    // por probar, vamos a hacer que sólo se renderice si la ruta es alfanumérica
    definePageMeta({
        validate: route => {
            // si la ruta no es alfanumérica, devolvemos false
            const regex = /^(?=.*[a-zA-Z!@#$%^&*_\-+=|\\()\[\]{};:'",.<>/?])[a-zA-Z0-9!@#$%^&*_\-+=|\\()\[\]{};:'",.<>/?]+$/;
            const expresion = new RegExp(regex);
            return expresion.test(route.params.title);
        }
    })
</script>

<template>
    <div>
        <!-- Al crear el fichero como [title], nuxt reemplaza las [...] por el nombre que le pasemos en la ruta -->
        <h1>Ruta con parámetros</h1>
        <h1>Parámetro 1: {{ route.params.title }}</h1>
        <h1>Parámetro 2: {{ route.params.category }}</h1>
    </div>
</template>