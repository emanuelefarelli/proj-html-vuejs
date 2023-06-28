<template>
    <section class="big-carousel">
        <div>
            <i class="fa-solid fa-chevron-left"
                @click="$emit('imgChange',false)"
            ></i>
            <i class="fa-solid fa-xmark"
                @click="$emit('carouselClose')"
            ></i>
            <img :src="getImagePath(imgList[activeIndex].img)" :alt="imgList[activeIndex].alt">
            <i class="fa-solid fa-chevron-right"
                @click="$emit('imgChange',true)"
            ></i>
        </div>
    </section>
</template>
    
<script>
    export default{
        name: 'FullCarousel',
        data(){
            return{
    
            }
        },
        methods:{
            getImagePath: function(img) {
                return new URL(`../assets/img/${img}`, import.meta.url).href;
            },
        },
        props: {
            imgList: Object,
            activeIndex: Number
        }
    }
</script>
    
<style lang="scss" scoped>
@use '../styles/partials/mixins.scss' as *;
@use '../styles/partials/variables.scss' as *;
    section.big-carousel{
        z-index: 1;
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100vh;
        background-color: rgba(0, 0, 0, 0.8);
        i{
            font-size: $FontSizeL;
            color: rgb(117, 117, 117);
        }
        i.fa-xmark{
            position: absolute;
            top: 220px;
            right: 550px;
            font-size: $FontSizeML;
        }
        i:hover{
            color: white;
        }
        div{
            @include flex();
            height: 100vh;
            img{
                width: 800px;
                margin: 0 20rem;
                box-shadow: rgba(50, 50, 93, 0.25) 0px 13px 27px -5px, rgba(0, 0, 0, 0.3) 0px 8px 16px -8px;
            }
        }
    }
</style>