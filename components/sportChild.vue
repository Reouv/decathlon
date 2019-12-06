<template>

    <div class="box-colonne">
        <div class="onglet">
            <h2>Sports : {{info.name}}</h2>
        </div>
        <div class="box-line">

            <div class="description-sport">
                <h1>{{info.name}}</h1>
                <p>{{info.description}}</p>
            </div>

            <div class="card menu scrollbar scrollbar-primary" >
                <div class="card-header">
                    <b>Liste des sous-sports</b>
                </div>
                <ul class="list-group list-group-flush">
                    <li class="list-group-item" v-for="child in childs">
                        {{child}}
                    </li>
                </ul>
            </div>
        </div>
        <b-button id="button-spt" variant="button-sport" @click="modifAffichage">Revenir a la liste des sports</b-button>


    </div>

</template>

<script>
    export default {
        props: {
            childs: null,
            info:null,
        },

        methods :{
            modifAffichage(){
                this.$parent.afficher = true
            }
        }

    }
</script>

<style>
    div.onglet{background-color: #575859;border-radius: 0px 0px 20px 20px;width: 100%;margin-left: 30%;}
    div.onglet h2{color: white;text-align: center;}

    div.box-colonne{width: 60%;display: flex;flex-direction: column;}
    div.box-colonne div.box-line{width: 100%;display: flex;flex-wrap: wrap;justify-content: space-around;padding: 20px;border-radius: 5px;background-color: rgba(0,0,0,0.5);margin-top: 10%;margin-left: 30%;}
    div.box-colonne div.box-line div.description-sport{width: 40%; border-radius: 10px;padding: 8px;}
    div.menu{max-height: 295px;overflow: auto;margin-top: 20px;}

    div.box-colonne h1{font-size: 1.2vw;text-align: center;color: white}
    div.box-colonne p{font-size: 1vw;text-align: justify;color: white}

    div.box-colonne #button-spt{max-width: 300px;border-radius: 5px;background-color: rgba(0, 0, 0, 0.7);color: white;transition: all 0.25s;border: #EAEAEA 1px solid;margin-top: 20px;margin-left: 30%;}
    div.box-colonne #button-spt:hover{box-shadow: 0 1px 5px black;background-color: rgba(0, 0, 0, 0.3);color: black}

    /* width */
    ::-webkit-scrollbar {
        width: 7px;
    }

    /* Track */
    ::-webkit-scrollbar-track {
        background: #B3B3B3;
        border-radius: 4px;
    }

    /* Handle */
    ::-webkit-scrollbar-thumb {
        background: #0076B4;
        border-radius: 4px;
    }

    /* Handle on hover */
    ::-webkit-scrollbar-thumb:hover {
        background: #555;
    }


</style>