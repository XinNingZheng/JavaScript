<template>
    <div>
        <transition-group name="." tag="ul" class="slide-box">
            <li class="slide-item" v-for="(img,index) in imgs" :key="index" v-show="index">
                <img :src="img"/>
            </li>  
        </transition-group>
    </div>    
</template>

<script>
    export default {
        props:['imgs'],
        data() {
            return {
                idx:0
            }
        },

    }
</script>

<style scope>
    .slide-box{
        position: relative;
    }
    .slide-item{
        position: absolute;
        left: 0;
        top: 0;
        width: 100%;
        height: 4rem;
    }
    /* .slide-item:first-child{
        z-index: 2;
    } */
    /* .slide-item:first-child{
        display: block;
    } */
    .slide-item img{
        width: 100%;
        height: 100%;
    }


</style>
