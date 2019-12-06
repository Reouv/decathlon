<template>

    <div class="box-banniere">
        <link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
        <div class="banniere">
            <img src="../assets/ban.png" alt="Pas d'image lol">
        </div>
        <div class="box-produits">

            <div class="produit">
                <img src="../assets/cyclisme.jpg" class="img-produit" alt="image sport">
                <div class="description">
                    <div class="text">
                        <p>Test micro test test test micro test</p>
                        <p>Test micro test test test micro test</p>
                    </div>
                    <div class="fleche">
                        <i class="material-icons" style="font-size:36px;">keyboard_arrow_right</i>
                    </div>

                </div>
            </div>


            <div class="produit">
                <img src="../assets/cyclisme.jpg" class="img-produit" alt="image sport">
                <div class="description">
                    <div class="text">
                        <p>Test micro test test test micro test</p>
                        <p>Test micro test test test micro test</p>
                    </div>
                    <div class="fleche">
                        <i class="material-icons" style="font-size:36px;">keyboard_arrow_right</i>
                    </div>

                </div>
            </div>


            <div class="produit">
                <img src="../assets/cyclisme.jpg" class="img-produit" alt="image sport">
                <div class="description">
                    <div class="text">
                        <p>Test micro test test test micro test</p>
                        <p>Test micro test test test micro test</p>
                    </div>
                    <div class="fleche">
                        <i class="material-icons" style="font-size:36px;">keyboard_arrow_right</i>
                    </div>

                </div>
            </div>

        </div>
    </div>
</template>


<script>
    import Logo from '~/components/Logo.vue'

    export default {
        components: {
            Logo
        }
    }
</script>

<style>
    div.box-banniere{width: 100%;display: flex;flex-wrap: wrap;justify-content: space-between;z-index: 1}
    div.box-banniere div.banniere{width: 60%;}
    div.box-banniere div.banniere img{width: 100%;}
    div.box-banniere div.box-produits {width: 40%; display: flex; flex-direction: column; justify-content: space-between}
    div.box-banniere div.produit{display: flex;width: 100%;max-height: 130px;}
    div.box-banniere div.box-produits div.produit{width: 100%;display: flex;flex-wrap: wrap;justify-content: space-between;}
    div.box-banniere div.box-produits div.produit img{display: block;width: 25%;}
    div.box-banniere div.box-produits div.produit div.description{width: 74%;margin: auto;display: flex;}
    div.box-banniere div.box-produits div.produit div.description p{font-size: 1.0vw;}
    div.box-banniere div.box-produits div.produit div.description div.text{width: 80%;}
    div.box-banniere div.box-produits div.produit div.description div.fleche{width: 20%;padding: 20px;}

    @media screen and (max-width : 1109px){
        div.box-banniere{width: 100%;display: flex;flex-wrap: wrap;flex-direction: column;}
        div.box-banniere div.banniere{width: 100%;}
        div.box-banniere div.banniere img{width: 100%;}
        div.box-banniere div.box-produits {width: 70%; display: flex; flex-direction: column; justify-content: space-between;margin: auto}
        div.box-banniere div.produit{display: flex;width: 100%;max-height: 130px;}
        div.box-banniere div.box-produits div.produit{width: 100%;display: flex;flex-wrap: wrap;justify-content: space-between;}
        div.box-banniere div.box-produits div.produit img{display: block;width: 25%;}
        div.box-banniere div.box-produits div.produit div.description{width: 74%;margin: auto;display: flex;}
        div.box-banniere div.box-produits div.produit div.description p{font-size: 1.0vw;}
        div.box-banniere div.box-produits div.produit div.description div.text{width: 40%;}
        div.box-banniere div.box-produits div.produit div.description div.fleche{width: 20%;padding: 20px;}
    }

</style>
