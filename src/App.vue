<template>    
    <Header/>
    <ListProducts/>
    <Rodape/>
</template>

<script lang="ts">
    import { defineComponent } from 'vue';
    import Header from './components/PageComponents/Header.vue';
    import ListProducts from './components/PageComponents/ListProducts.vue';
    import Rodape from './components/PageComponents/Rodape.vue';
    
    export default defineComponent({
        name: 'App',
        components: {
            Header,
            ListProducts,
            Rodape
        }
    });
</script>

<style>
    #app {
        font-family: Avenir, Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
    }
</style>
