<template>
    <section class="jumbotron">
        <div class="box">
            <p class="banner">
                welcome
            </p>
            <h1>
                academic chess for <span>everyone</span>
            </h1>
            <p>
                We are dedicated to broadening and developing chess as art, recreation, and as a significant element of culture in Northern California.
            </p>
            <div class="button">
                <button class="enroll">
                    Enroll Now
                </button>
                <button class="learn">
                    Learn More
                </button>
            </div>
        </div>
    </section>
</template>
    
<script>
    export default{
        name: 'AppJumbotron',
        data(){
            return{
    
            }
        },
    }
</script>
    
<style lang="scss" scoped>
@use '../styles/partials/mixins.scss' as *;
@use '../styles/partials/variables.scss' as *;
    section.jumbotron{
        height: 85vh;
        background-image: url(../assets/img/mt-2236-home-bg1.jpg);
        background-size: cover;
        div.box{
            @include marginAuto;
            @include flex(column,center,flex-start);
            height: 100%;
            padding-right: 30%;
            width: $dimension;
            p.banner,
            h1{
                text-transform: uppercase;
            }
            p.banner{
                font-size: $FontSizeXS;
                font-weight: 300;
                background-color: $yellowColor;
                padding: 0.1rem 0.7rem;
                border-radius: 1rem;
                color: black;
            }
            h1{
                font-size: $FontSizeXL;
                font-weight: 600;
                color: white;
                span{
                    color: $yellowColor;
                    font-style: italic;
                }
            }
            p{
                color: white;
                font-size: $FontSizeM;
                padding: 2rem 0;
            }
            button{
                padding: 1rem 3rem;
                margin: 0.5rem;
                border: none;
                border-radius: 0.5rem;
                font-size: $FontSizeM;
            }
            button.enroll{
                background-color: $yellowColor;
                border: 3px solid $yellowColor;
            }
            button.enroll:hover{
                background-color: $darkGreyColor;
                border: 3px solid $darkGreyColor;
                color: white;
            }
            button.learn{
                background-color: rgba(0, 0, 0, 0);
                color: white;
                border: 3px solid white;
            }
            button.learn:hover{
                background-color: $yellowColor;
                color: black;
                border: 3px solid $yellowColor;
            }
        }
        div.button{
            @include flex();
        }
    }
</style>