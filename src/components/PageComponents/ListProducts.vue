<template lang="">
    <div class="container-fluid list">        
        <div class="container mb-5">
            <div class="highlights">
                Produtos em Destaque
            </div>
            <div class="row">      
                <div class="col-12 col-md-4" v-for="(product, index) in highlights" :key="index+9999">         
                    <Product :product="product"/>                
                </div>
            </div>
        </div>
        <div class="container">
            <div class="highlights">
                Mais Produtos
            </div>
            <div class="row">      
                <div class="col-12 col-md-4" v-for="(product, index) in products" :key="index">         
                    <Product :product="product"/>                
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import { defineComponent, onMounted, ref } from "vue"
    import Product from './Product.vue';
    import api from '@/services/api';

    export default defineComponent({
        nome: "ListProducts",
        components: {
            Product
        },
        setup(){
            const products = ref([]);
            const highlights = ref([]);

            const fetchProducts = () => api.get('/products').then((response) => {
                products.value = response.data.data
            });
            
            const fetchHighlights = () => api.get('/highlights').then((response) => {
                highlights.value = response.data.data
            });
            
            onMounted(fetchProducts);
            onMounted(fetchHighlights);

            return { products, highlights }
        }
    })
</script>

<style scoped>
    .list{
        padding-bottom: 100px;
    }
    .highlights{
        text-align: left;
        font-weight: bold;
        font-size: 20px;
        color: #777;
        border: 1px solid #777;
        font-family: 'Montserrat', sans-serif;
        padding: 20px 30px;
        margin-bottom: 40px;
        border-radius: 10px;
    }
</style>