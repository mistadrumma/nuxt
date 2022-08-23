<template>
    <nav class="navbar navbar-expand-lg bg-light">
    <div class="container-fluid">
        <a class="navbar-brand" href="/">Nuxt App</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav me-auto mb-2 mb-lg-0">
            <li class="nav-item">
                <nuxt-link no-prefetch exact active-class="active" class="nav-link" aria-current="page" to="/">
                    Home
                </nuxt-link>
            </li>
            <li class="nav-item">
                <nuxt-link no-prefetch active-class="active" class="nav-link" aria-current="page" to="/about">
                    About
                </nuxt-link>
            </li>
            <li class="nav-item">
                <nuxt-link no-prefetch active-class="active" class="nav-link" aria-current="page" to="/users">
                    Users
                </nuxt-link>
            </li>
        </ul>
        </div>
    </div>
    </nav>       
</template>             