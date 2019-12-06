<template>
    <div style="display: flex;align-items: center;justify-content: center;">
        <video controls muted id="videoID" ref="video" v-show="affichage" width="1000" height="800">
            <source src="../../assets/troll.mp4" type="video/mp4">
            Your browser does not support the video tag.
        </video>
        <b-button variant="outline-primary" @click="test" ref="button" v-show="!affichage" style="margin-top: 50vh">Cliquer ici pour charger le catalogue
        </b-button>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                affichage: false
            }
        },
        mounted() {
            console.log(this.$refs.play)

        },

        methods: {

            test() {
                this.affichage = true
                this.$refs.video.muted = false
                this.$refs.video.play()
            }
        }
    }
</script>