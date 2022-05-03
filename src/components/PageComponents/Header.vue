<template lang="">
    <header>
        <div class="page-header">
            <div class="container">
                <div class="row">
                    <div class="col-xl-12 col-lg-12 col-md-12 col-sm-12 col-12">
                        <div class="page-caption">
                            <h1 class="page-title"></h1>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="card-section">
            <div class="container">
                <div class="card-block bg-white mb30">
                    <div class="row">
                        <div class="col-xl-12 col-lg-12 col-md-12 col-sm-12 col-12">
                            <div class="section-title mb-0">
                                <NavBar/>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </header>
</template>

<script>
    import { defineComponent } from "vue"
    import NavBar from './NavBar.vue'

    export default defineComponent({
        nome: "Header",
        components: {
            NavBar
        }
    })
</script>

<style scoped>
    h1, h2, h3, h4, h5, h6 { 
        color: #25292a; 
        margin: 0px 0px 10px 0px; 
        font-family: calibri light; 
        font-weight: 700;         
        line-height: 1; 
    }
    h1 { 
        font-size: 34px; 
        letter-spacing: 1px; 
        text-shadow: 0px 0px 16px black;
    }
    h2 { 
        font-size: 28px; line-height: 38px; 
    }
    h3 { 
        font-size: 22px; line-height: 32px; 
    }
    h4 { 
        font-size: 20px; 
    }
    h5 { 
        font-size: 17px; 
    }
    h6 { 
        font-size: 12px; 
    }
    p { 
        margin: 0 0 20px; line-height: 1.7; 
    }
    p:last-child { 
        margin: 0px; 
    }
    a { 
        text-decoration: none; 
        color: #8d8f90; 
        -webkit-transition: all 0.3s; 
        -moz-transition: all 0.3s; 
        transition: all 0.3s; 
    }
    a:focus, a:hover { 
        text-decoration: none; 
        color: #f85759; 
    }
    .page-header { 
        background: url('../../assets/img/banner_01.jpg')no-repeat; 
        position: relative; 
        background-size: cover; 
    }
    .page-caption { 
        padding-top: 170px; 
        padding-bottom: 174px; 
    }
    .page-title { 
        font-size: 46px; 
        line-height: 1; 
        color: #fff; 
        font-weight: 600; 
        text-align: center; 
    }

    .card-section { 
        position: relative; 
        bottom: 320px; 
        
    }
    .card-block { 
        padding: 20px; 
        box-shadow: 0px 5px 5px rgba(0, 0, 0, 0.2);
        border-radius: 10px;
    }
    .section-title { 
        margin-bottom: 60px; 
    }
</style>