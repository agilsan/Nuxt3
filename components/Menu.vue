<template>
    <nav class="navbar navbar-expand-lg bg-body-tertiary">
        <div class="container-fluid">
            <a class="navbar-brand" href="#">Nuxt 3</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
                aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav">
                    <li class="nav-item">
                        <!-- con esto nos movemos por las distintas páginas -->
                        <NuxtLink :to="{ name:'index' }" class="nav-link" active-class="active">Home</NuxtLink>
                    </li>
                    <li class="nav-item">
                        <!-- con esto nos movemos por las distintas páginas -->
                        <NuxtLink :to="{ name: 'products' }" class="nav-link" active-class="active">Products</NuxtLink>
                    </li>
                    <li class="nav-item">
                        <!-- con esto nos movemos por las distintas páginas -->
                        <NuxtLink :to="{ name: 'contacto' }" class="nav-link" active-class="active">Contacto</NuxtLink>
                    </li>
                    <li class="nav-item">
                        <!-- con esto nos movemos por las distintas páginas -->
                        <NuxtLink :to="{ name: 'account' }" class="nav-link" active-class="active">Account</NuxtLink>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
</template>

<style scoped>
.active {
    border-bottom: 2px solid purple;
}
</style>