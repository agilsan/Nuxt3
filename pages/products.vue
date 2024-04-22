<script setup>
/**
 * useFetch lo utilizamos cuando queremos cargar datos de manera asíncrona, pero la petición es menos pesada
 */
// const { data, pending, error } = await useFetch('https://dummyjson.com/products',{
//     lazy: true,
//     pick: ['products']
// });

/**
 * useAsyncData es para cargar datos de forma asincrona igual que el anterior, pero permite más opciones
 * se utiliza cuando la carga de datos es muy pesada y se quiere que se cargue solo cuando se necesite
 * bloquea la navegación, hasta que la petición ha terminado
 */
 const { data, pending, error } = await useAsyncData(
     'products',
     () => $fetch('https://dummyjson.com/products'), {
        pick: ['products'],
        lazy: true
     }
 );

</script>

<template>
    <div>
        <div class="spinner-border" role="status" v-if="pending">
            <span class="visually-hidden">Loading...</span>
        </div>
        <div v-else>
            <h1>Page products</h1>
            <div class="grid">
                <Card v-for="product in data.products" :key="product.id" :product="product" :style="'width: 18rem;'" />
            </div>
        </div>
    </div>
</template>

<style scoped>
.grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(18rem, 1fr));
    gap: 2rem;
}
</style>