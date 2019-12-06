<template>
    <div>
        <header>
            <img src="../assets/logo_decathlon.jpg" alt="logo Décathlon" class="img_logo" @click="redirect">
        </header>
    </div>
</template>

<style scoped>
    img{
    cursor: pointer;
    }
    header {
        width: 100%;
        height: 80px;
        top: 0;
        background-color: rgba(35, 35, 35, 1);
        box-shadow: 0px 3px 5px black;
        margin-bottom: 3px;
    }

    header img.img_logo{
        max-height: 80px;
        display: block;
        margin: auto;
    }
</style>

<script>
    export default {
        methods :
            {
                redirect(){
                    this.$router.push("/")
                }
            }

    }
</script>