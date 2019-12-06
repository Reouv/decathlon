<template>
    <div>

        <div class="row" v-if="afficher">
            <div v-for="sport in sports" class="test col-sm-2">
                <div class="card" style="width: 18rem;">
                    <img :src="sport.attributes.icon" alt="" width="50px">
                    <div class="card-body" >
                        <h5 class="card-title">{{sport.attributes.name}}</h5>
                        <p class="card-text">{{sport.attributes.description}}</p>
                        <b-button @click="affichageSwitch(sport.relationships.tags.data)"variant="primary">Plus d'infos</b-button>
                    </div>
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

</style>

<script>
    import sportChild from "../../components/sportChild";
    export default {
        components:{
            sportChild
        },

        data() {
            return {
                afficher:true,
                sports: null,
                childData:null,
            }
        },

        mounted() {
            this.$axios.get("https://sports.api.decathlon.com/sports")
                .then((response) => {
                    console.log(response)
                    this.sports = response.data.data

                })
        },
        methods:{
            affichageSwitch(value){
                this.childData = value
                this.afficher = false

            }
        }
    }
</script>