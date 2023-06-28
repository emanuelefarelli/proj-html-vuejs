<template>
    <section class="first-step">
        <div class="container">
            <div>
                <h1>
                    take the <span>first step</span> 
                </h1>
                <p>
                    The fascinating world of chess has its doors open for anyone
                </p>
            </div>
            <button>
                View More
            </button>
        </div>
    </section>
</template>
    
<script>
    export default{
        name: 'AppFirstStep',
        data(){
            return{
    
            }
        },
    }
</script>
    
<style lang="scss" scoped>
@use '../styles/partials/mixins.scss' as *;
@use '../styles/partials/variables.scss' as *;
    section.first-step{
        height: 32vh;
        background-image: url(../assets/img/mt-2236-home-bg2.jpg);
        background-size: cover;
        div.container{
            @include marginAuto;
            @include flex(row,space-between,center);
            width: $dimension;
            height: 100%;
            color: white;
            h1{
                text-transform: uppercase;
                font-size: $FontSizeL;
                margin-bottom: 1.5rem;
                span{
                    color: $yellowColor;
                }
            }
            p{
                font-size: $FontSizeM;
                font-weight: 300;
            }
            button{
                background-color: $yellowColor;
                font-size: $FontSizeM;
            }
            button:hover{
                background-color: $darkGreyColor;
                color: white;
            }
        }
    }
</style>