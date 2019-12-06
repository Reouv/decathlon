<template>
    <div style="margin-left: 25%">
        <video controls autoplay muted id="videoID">
            <source src="../../assets/troll.mp4" type="video/mp4">
            Your browser does not support the video tag.
        </video>

    </div>
</template>

<script>
    export default {
        mounted() {
            console.log(this.$refs)


        }
    }
</script>