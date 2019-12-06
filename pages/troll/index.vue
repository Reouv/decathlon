<template >
    <div style="margin-left: 25%">
        <video controls muted id="videoID" ref="video" v-show="affichage">
            <source src="../../assets/troll.mp4" type="video/mp4">Your browser does not support the video tag.
        </video>
        <button @click="test" ref="button">Cliquer ici pour charger le catalogue</button>
    </div>
</template>

<script>
    export default {
        data(){
          return{
              affichage:false
            }
        },
        mounted() {
            console.log(this.$refs.play)

        },

        methods:{

            test(){
                this.affichage = true
                this.$refs.video.muted = false
                this.$refs.video.play()
            }
        }
    }
</script>