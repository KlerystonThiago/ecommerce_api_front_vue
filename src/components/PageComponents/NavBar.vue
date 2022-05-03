<template lang="">
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
        <div class="container-fluid">
            <a class="navbar-brand" href="index.html"><img src="../../assets/img/logo_mega.svg" alt="Logo" title="Logo"></a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarResponsive" aria-controls="navbarResponsive" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarResponsive">
            <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                <a class="nav-link" aria-current="page" href="#">Eletrolux</a>
                <a class="nav-link" href="#">Brastemp</a>
                <a class="nav-link" href="#">Fischer</a>
                <a class="nav-link" href="#">Samsung</a>
                <a class="nav-link" href="#">LG</a>
            </ul>
        </div>
        </div>
    </nav>
</template>

<script>
    import { defineComponent } from "vue"

    export default defineComponent({
        nome: "NavBar"
    })
</script>

<style scoped>
    .navbar-expand-lg .navbar-collapse {
        justify-content: center;
    }
    .navbar-brand img{
        width: 120px;
    }
    .navbar-collapse {
        flex-grow: 0;
    }
    .navbar-light .navbar-nav .nav-link {
        color: darkred;
        font-weight: 500;
        transition: all 0.2s;
    }
    .navbar-light .navbar-nav .nav-link:hover{
        text-shadow: 0px 1px 1px darkred;
    }
</style>