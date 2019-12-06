<template>
    <div>
        <div class="card" style="width: 18rem;">
            <div class="card-header">
                Liste des sous-sports
            </div>
            <ul class="list-group list-group-flush">
                <li class="list-group-item" v-for="child in childs">
                    {{child}}
                </li>
            </ul>
        </div>
        <b-button variant="outline-primary" @click="modifAffichage">Revenir a la liste des sports</b-button>
    </div>

</template>

<script>
    export default {
        props: {
            childs: null,
        },

        methods :{
            modifAffichage(){
                this.$parent.afficher = true
            }
        }

    }
</script>