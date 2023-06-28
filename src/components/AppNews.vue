<template>
    <section class="news">
        <div class="container">
            <div>
                <h1>
                    Latest News
                </h1>
                <hr>
                <button>
                    View Other Posts
                </button>
            </div>
            <div>
                <img src="../assets/img/mt-2236-blog-img1.jpg" alt="Chess player Junior">
                <p>The most common mistakes when managing personal finances</p>
            </div>
            <div>
                <img src="../assets/img/mt-2236-blog-img2.jpg" alt="Chess player Junior">
                <p>Methods of the recruitment</p>
            </div>
        </div>
    </section>
</template>
    
<script>
    export default{
        name: 'AppNews',
        data(){
            return{
    
            }
        },
    }
</script>
    
<style lang="scss" scoped>
@use '../styles/partials/mixins.scss' as *;
@use '../styles/partials/variables.scss' as *;
    section.news{
        height: calc(65vh - 4.5rem);
        background-color: $lightGreyColor;
        div.container{
            @include flex();
            @include marginAuto;
            height: 100%;
            width: $dimension;
            div{
                width: calc(100% / 3);
                height: 300px;
                padding: 1rem;
                h1{
                    font-size: $FontSizeL;
                }
                button{
                    background-color: $lightGreyColor;
                    border: 2px solid $darkGreyColor;
                    font-size: $FontSizeM;
                }
                button:hover{
                    background-color: $darkGreyColor;
                    color: white;
                }
                hr{
                    width: 90px;
                    border: 2px solid $yellowColor;
                    margin: 2rem 0;
                }

                img{
                    width: 100%;
                }
                p{
                    font-size: $FontSizeM;
                    font-weight: 300;
                }
                p:hover{
                    cursor: pointer;
                    color: $yellowColor;
                }
            }
        }
    }
</style>