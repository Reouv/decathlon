<template>
    <div>

        <div class="row col-container" v-if="afficher">
            <div v-for="sport in sports" class="test col-sm-2 col">
                <div class="card contenuPrixTitreGrandeJacquette " style="width: 18rem;height: 100%">
                    <img :src="sport.attributes.icon" alt="" width="100px">
                    <div class="card-body">
                        <h5 class="card-title">{{sport.attributes.name}}</h5>
                        <p class="card-text">{{sport.attributes.description}}</p>
                    </div>
                    <b-button @click="affichageSwitch(sport.relationships.tags.data)" variant="primary" class="bouton-down">Plus d'infos</b-button>
                </div>
                <br>
            </div>

        </div>
        <div v-else>
            <sportChild :childs="childData"/>
        </div>

    </div>
</template>

<style>

    .bouton-down {
        width: 70%;
        align-self: center;
        margin-bottom: 10px;
    }

    .col-container {
        display: flex;
        width: 100%;

    }

    .col {
        flex: 1;
        padding: 16px;
        width: 70vh;
    }

</style>

<script>
    import sportChild from "../../components/sportChild";

    export default {
        components: {
            sportChild
        },

        data() {
            return {
                afficher: true,
                sports: null,
                childData: null,
            }
        },

        mounted() {
            this.$axios.get("https://sports.api.decathlon.com/sports")
                .then((response) => {
                    this.sports = response.data.data
                })
        },
        methods: {
            affichageSwitch(value) {
                this.childData = value
                this.afficher = false
            }
        }
    }
</script>