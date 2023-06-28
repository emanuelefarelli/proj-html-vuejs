<template>
    <section class="events">
        <h1>
            Our Events
        </h1>
        <p>
            Chess is fun and we are happy to prove it at our events!
        </p>
        <div class="container">
            <img src="../assets/img/mt-2236-home-img4.jpg" alt="Image of Summer Tournament">
            <div>
                <h2>
                    Grand Summer Tournament of  2021
                </h2>
                <p>
                    Join us for the Grand Summer Tournament 2021. Held every year on the first Sunday of summer, our Grand Summer Tournament chess masters and beginners from North California.
                    We have competitions for different levels of chess mastery with amazing prizes awarded at each level.
                </p>
            </div>
            <button>
                Register
            </button>
        </div>
        <div class="container">
            <img src="../assets/img/mt-2236-home-img5.jpg" alt="Image of Summer Tournament">
            <div>
                <h2>
                    World Chess Day
                </h2>
                <p>
                    Celebrated on July 20 every year, World Chess Day is one of the biggest events at our school. Be ready for fun tournaments and big prizes. Registration is obligatory!
                </p>
            </div>
            <button>
                Register
            </button>
        </div>
    </section>
</template>
    
<script>
    export default{
        name: 'AppEvents',
        data(){
            return{
    
            }
        },
    }
</script>
    
<style lang="scss" scoped>
@use '../styles/partials/mixins.scss' as *;
@use '../styles/partials/variables.scss' as *;
    section.events{
        @include flex(column);
        height: 90vh;
        h1,
        p{
            margin-bottom: 1.5rem ;
        }
        h1{
            font-size: $FontSizeL;
        }
        p{
            font-size: $FontSizeML;
            font-weight: 300;
        }
        div.container{
            @include flex(row,space-between,center);
            width: $dimension;
            margin-top: 3rem;
            img{
                width: 30%;
            }
            h2{
                font-size: $FontSizeML;
                margin-bottom: 1.5rem;
            }
            div{
                width: 40%;
            }
            p{
                font-size: $FontSizeS;
                line-height: 1.4rem;
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