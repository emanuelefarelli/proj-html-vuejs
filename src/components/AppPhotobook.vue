<template>
    <FullCarousel v-if="FullScreenImgs === true"
        :imgList = "imgList"
        :activeIndex = "activeIndex"
        @imgChange="changeActiveIndex"
        @carouselClose="this.FullScreenImgs = false"
    />
    <section class="photobook">
        <div class="carousel">
            <div class="thumbnail" v-for="imgObj in imgList">
                <img :src="getImagePath(imgObj.img)" :alt="imgObj.alt" @click="openFullScreenImg(imgObj.index)">
            </div>
        </div>
        <div class="start-learn">
            <div>
                <img src="../assets/img/mt-2236-home-icon5.png" alt="Home horse icon">
            </div>
            <div>
                <h1>
                    play & learn
                </h1>
                <p>
                    Take a look into our day to day life here at Chess School 
                </p>
            </div>
            <div>
                <button>
                    Learn More
                </button>
            </div>
        </div>
    </section>
</template>
    
<script>
    import FullCarousel from './FullCarousel.vue';

    export default{
        name: 'AppPhotobook',
        data(){
            return{
                imgList: [
                    {
                        img: 'mt-2236-home-gallery1.jpg',
                        alt: 'White is playing against black',
                        index: 0,
                    },
                    {
                        img: 'mt-2236-home-gallery2.jpg',
                        alt: 'A black pedestrian inside white pieces',
                        index: 1,
                    },
                    {
                        img: 'mt-2236-home-gallery3.jpg',
                        alt: 'Childs play chess',
                        index: 2,
                    },
                    {
                        img: 'mt-2236-home-gallery4.jpg',
                        alt: 'Chess view',
                        index: 3,
                    },
                ],
                activeIndex: 0,
                FullScreenImgs: false,
            }
        },
        methods: {
            getImagePath: function(img) {
                return new URL(`../assets/img/${img}`, import.meta.url).href;
            },
            openFullScreenImg(index){
                this.activeIndex = index;
                this.FullScreenImgs = true;
                console.log(this.activeIndex);
                console.log(this.FullScreenImgs);
            },
            changeActiveIndex(direction){
                if(direction === true){
                    this.activeIndex++;
                    if(this.activeIndex > 3){
                        this.activeIndex = 0;
                    }
                }else{
                    this.activeIndex--;
                    if(this.activeIndex < 0){
                        this.activeIndex = 3;
                    }
                }
            }
        },
        components:{
            FullCarousel
        }
    }
</script>
    
<style lang="scss" scoped>
@use '../styles/partials/mixins.scss' as *;
@use '../styles/partials/variables.scss' as *;
    section.photobook{
        height: 50vh;
        div.carousel{
            @include flex();
            div.thumbnail{
                width: calc(100% / 4);
                img{
                    width: 100%;
                }
            }
        }
        div.start-learn{
            @include flex();
            background-color: $yellowColor;
            height: 200px;
            div{
                margin: 2rem;
                h1{
                    font-size: $FontSizeL;
                    text-transform: uppercase;
                }
                p{
                    font-size: $FontSizeM;
                    margin-top: 1.5rem;
                }
                button{
                    font-size: $FontSizeM;
                    border: 2px solid black;
                    background-color: $yellowColor;
                }
                button:hover{
                    border: 2px solid $darkGreyColor;
                    background-color: $darkGreyColor;
                    color: white;
                }
            }
        }
    }
</style>