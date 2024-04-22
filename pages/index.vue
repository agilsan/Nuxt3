<script setup>
    const { data, pending, error } = await useFetch('https://dummyjson.com/products/1',{
        lazy: true
    });
</script>

<template> <!-- Dentro de la carpeta pages, si creamos un fichero index.vue, nuxt lo toma como la página de inicio -->
    <div>
        <div class="spinner-border" role="status" v-if="pending">
            <span class="visually-hidden">Loading...</span>
        </div>
        <div v-else>
            <h1>Sale product</h1>
            <div class="container">
                <Card :key="data.id" :product="data" :style="''" />
            </div>
        </div>
    </div>
</template>