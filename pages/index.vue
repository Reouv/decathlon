<template>
    <div class="wrapper">
        <div class="div1">
            <img src="../assets/Banniere.jpeg" alt="Pas d'image lol" width="101%">
        </div>
        <div class="div2">
            <b-container class="bv-example-row bv-example-row-flex-cols" fluid>
                <b-row>
                    <b-col align-self="end">
                        <div id=contenu>
                            <span>Les nouveaux sports</span>
                        </div>
                    </b-col>
                </b-row>
                <b-row>
                    <b-col align-self="end">
                        <div class="selector2">
                        </div>
                    </b-col>
                </b-row>
                <b-row>
                    <b-col align-self="end">
                        <div class="selector3">
                        </div>
                    </b-col>
                </b-row>
            </b-container>
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

    #contenu:hover{
        background-color: #c3c7d1;
    }
    #contenu{
        font:Verdana, Geneva, sans-serif;
        font-size:18px;
        text-align:center;
        height:16vh;
        display: table;
        width: 100%;
    }
    #contenu span {
        /* Aligne le texte verticalement au milieu */
        vertical-align:middle;
        display: table-cell;
    }

    .selector1 {
        width: 100%;
        height: 16vh;
    }
    .selector2 {
        background-color: purple;
        width: 100%;
        height: 15vh;
    }
    .selector3 {
        background-color: blue;
        width: 100%;
        height: 15vh;
    }

    .div1 {
        width: 60%;
        height: 50vh;
        float: left;
        position: relative;

    }

    .div2 {
        width: 40%;
        height: 50vh;
        float: left;
        position: relative;

    }

    .container {
        margin: 0 auto;
        min-height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
    }

    .title {
        font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
        'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
        display: block;
        font-weight: 300;
        font-size: 100px;
        color: #35495e;
        letter-spacing: 1px;
    }

    .subtitle {
        font-weight: 300;
        font-size: 42px;
        color: #526488;
        word-spacing: 5px;
        padding-bottom: 15px;
    }

    .links {
        padding-top: 15px;
    }
</style>
