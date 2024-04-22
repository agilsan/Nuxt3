 <!-- 
    El layout principal tiene que llamarse default.vue 
    Los layout deben contener piezas de interfaz común a varias páginas. Por ejemplo. un menú de navegación
    También tenemos que tener un espacio de página dinámico, donde se va a renderizar la página que se está visitando. Esto se hace con un slot
-->
<template>
    <Menu />
    <div class="container">
        <slot />
    </div>
</template>