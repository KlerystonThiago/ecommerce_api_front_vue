<template lang="">
    <footer>
        <div class="row">
            <div class="col-12 col-md-4 fs-8">   

            </div>
            <div class="col-12 col-md-4"> 
                <p>{{ new Date().getFullYear() }} Kleryston Thiago Todos os Direitos Reservados</p>           
            </div>
            <div class="col-12 col-md-4">
            <p>
                <i class="fa-brands fa-linkedin"></i>
                <i class="fa-brands fa-instagram-square"></i>
                <i class="fa-brands fa-facebook"></i>
            </p>            
            </div>
        </div>
    </footer>
</template>

<script>
    import { defineComponent } from "vue"

    export default defineComponent({
        nome: "Rodape"
    })
</script>

<style scoped>
    footer{
        width: 100%;
        min-height: 10px;
        background-color: #222;
        color: white;
        padding: 20px;
    }

    footer p{
        margin:0;
        padding: 0;
    }
    
    footer i{
        margin:0;
        padding: 0;
        font-size: 20px;
    }

    .fa-instagram-square{
        margin-left: 20px;
        margin-right: 20px;        
    }

    .fs-8{
        font-size: 13px;
    }
</style>