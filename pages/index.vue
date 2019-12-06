<template>
    <div class="box-banniere">
        <div class="banniere">
            <img src="../assets/ban.png" alt="Pas d'image lol">
        </div>
        <div class="box-produits">

            <div class="produit">
                <img src="../assets/cyclisme.jpg" class="img-produit" alt="image sport">
                <div class="description">
                    <p>Okay okay just a test</p>
                    <p>Okay okay just a test</p>
                </div>
            </div>


            <div class="produit">
                <img src="../assets/cyclisme.jpg" class="img-produit" alt="image sport">
                <div class="description">
                    <p>Okay okay just a test</p>
                    <p>Okay okay just a test</p>
                </div>
            </div>


            <div class="produit">
                <img src="../assets/cyclisme.jpg" class="img-produit" alt="image sport">
                <div class="description">
                    <p>Okay okay just a test</p>
                    <p>Okay okay just a test</p>
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
    div.box-banniere{width: 100%;display: flex;flex-wrap: wrap;justify-content: space-between;}
    div.box-banniere div.banniere{width: 59%;}
    div.box-banniere div.banniere img{width: 100%;}
    div.box-banniere div.box-produits {width: 40%;}
    div.box-banniere div.produit{display: flex;width: 100%;max-height: 130px;}
    div.box-banniere div.box-produits div.produit{width: 100%;display: flex;flex-wrap: wrap;justify-content: space-between;}
    div.box-banniere div.box-produits div.produit img{display: block;width: 30%;}
    div.box-banniere div.box-produits div.produit div.description{width: 65%;}
</style>
