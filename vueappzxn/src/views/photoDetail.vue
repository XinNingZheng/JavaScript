<template>
    <div>

        <!-- <img :src="url"/> -->
        <div class="img-box" :style="{backgroundImage:'url('+url+')'}"></div>

    </div>
</template>

 
<script>
export default{
    computed: {
        url(){
            // http://localhost:8080/img/photo/1.jpg
            return this.$store.state.photoData[this.$route.params.index].src
        }
    },
}

</script> 

<style scoped>
.img-box{
    position: absolute;
    left: 0;
    top: 1rem;
    bottom: 1rem;
    right: 0;
    background: rgb(0, 0, 0) 0 center no-repeat;
    background-size: contain;
}
</style>

