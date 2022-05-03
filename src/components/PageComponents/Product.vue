<template lang="">
    <div class="box-product">
        <div>
            <i class="fa-regular fa-heart like"></i>
            <img :src="`${this.baseUrlProduct+product.image}`" />        
            <p>
                <i class="fa-solid fa-star star"></i>
                <i class="fa-solid fa-star star"></i>
                <i class="fa-solid fa-star star"></i>
                <i class="fa-solid fa-star"></i>
                <i class="fa-solid fa-star"></i>
            </p>
            <p>{{product.name}}</p>
            <strong>{{product.formatted_price}}</strong>
        </div>        
        <div>            
            <p>
                <button class="btn btn-primary">more details</button>
            </p>
        </div>
    </div>
</template>

<script lang="ts">
    import { defineComponent, PropType } from "vue"
    import IProduct from '../../Interfaces/IProduct'

    export default defineComponent({
        nome: "Product",
        props: {
            product: {
                type: Object as PropType<IProduct>,
                required: true
            }
        },
        data(){
            return {
                baseUrlProduct: 'http://localhost:8000/'
            }
      },
    })
    
</script>

<style scoped>
    .box-product{
        width: 100%;
        height: 100%;
        position: relative;
        padding: 10px;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        padding-bottom: 50px;
    }

    .box-product img{
        width: 70%;
        margin: 0px auto;
    }
    
    .box-product p{
        padding: 0;
        margin: 0;
    }
    
    .box-product i{
        letter-spacing: 2px;
        font-size: 12px;
        color: #999;
    }
    
    .box-product button{
        background-color: #6284ce;
        margin-top: 10px;
        padding-left: 20px;
        padding-right: 20px;
        transition: all 0.2s linear;
    }

    .box-product button:hover{
        background-color: #333;
        border-color: #333;
    }
    
    .box-product strong{
        font-size: 20px;
        color: #666;
    }

    .star{
        color: gold !important;
    }

    .like{
        position: absolute;
        font-size: 20px !important;
        margin: 0px auto;
        z-index: 2;
    }

    .box-product{
        
         
        
    }
</style>