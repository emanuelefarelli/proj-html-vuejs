<template>
    <section class="services">
        <h1>
            our services
        </h1>
        <p>
            We make your child happy day after day
        </p>
        <div class="box">
            <div>
                <h3>
                    Chess Education
                </h3>
                <p class="subtitle">
                    Popular education for your child and you
                </p>
                <p>
                    Teachers and parents around the world know that chess is not a simple game. It is a great learning tool that will help build your child’s executive function skills.
                </p>
                <ul>

                    <li>
                        <img src="../assets/img/mt-2236-home-icon-bullet.png" alt="Icon for list">
                        <span> Build self-regulation and motivation </span>
                    </li>
                    <li>
                        <img src="../assets/img/mt-2236-home-icon-bullet.png" alt="Icon for list">
                        <span> Help with concentration issues </span>
                    </li>
                    <li>
                        <img src="../assets/img/mt-2236-home-icon-bullet.png" alt="Icon for list">
                        <span> Learn to plan, organize, and prioritize </span>
                    </li>
                    <li>
                        <img src="../assets/img/mt-2236-home-icon-bullet.png" alt="Icon for list">
                        <span> Regulate emotions </span>
                    </li>
                    <li>
                        <img src="../assets/img/mt-2236-home-icon-bullet.png" alt="Icon for list">
                        <span> Learn to pay attention to detail </span>
                    </li>
                </ul>
                <button>
                    Learn More
                </button>
            </div>
            <div>
                <div class="variant">
                    <img src="../assets/img/mt-2236-home-icon1.png">
                    <h2>
                        Various Age Groups
                    </h2>
                    <p>
                        We provide chess classes to both children from 5 years old and adults.
                    </p>
                </div>
                <div class="variant">
                    <img src="../assets/img/mt-2236-home-icon3.png" alt="Groups icon">
                    <h2>
                        Best Chess Players
                    </h2>
                    <p>
                        Our alumni have won many prestigious chess tournaments in the country.
                    </p>
                </div>
            </div>
            <div>
                <div class="variant">
                    <img src="../assets/img/mt-2236-home-icon2.png" alt="Groups icon">
                    <h2>
                        Top Chess Variants
                    </h2>
                    <p>
                        We don’t only teach classical chess but also other top variants of this game.
                    </p>
                </div>
                <div class="variant">
                    <img src="../assets/img/mt-2236-home-icon4.png" alt="Groups icon">
                    <h2>
                        Best Chess Openings
                    </h2>
                    <p>
                        Our students know all the best chess openings and how to use them.
                    </p>
                </div>
            </div>
        </div>
    </section>
</template>
    
<script>
    export default{
        name: 'AppServices',
        data(){
            return{
    
            }
        },
    }
</script>
    
<style lang="scss" scoped>
@use '../styles/partials/mixins.scss' as *;
@use '../styles/partials/variables.scss' as *;
    section.services{
        @include marginAuto;        
        @include flex(column);
        width: $dimension;
        height: 80vh;
        line-height: 1.3rem;
        h1,
        p{
            margin-bottom: 2rem;
        }
        h1{
            text-transform: uppercase;
            font-size: $FontSizeL;
        }
        p{
            font-size: $FontSizeML;
            font-weight: 300; 
        }
        div.box{
            @include flex();
            width:100%;
            h3,
            p{
                margin-bottom: 1rem;
            }
            h3{
                font-size: $FontSizeML;
            }
            p.subtitle{
                font-size: $FontSizeML;
            }
            div{
                width: calc(100% / 3);
                padding: 0 2rem;
                p{
                    font-size: $FontSizeS;
                }
                ul li{
                    margin-bottom: 0.8rem;
                    span{
                        font-weight: 300;
                    }
                    img{
                        margin: 0 0.8rem;
                    }
                }
                button{
                    background-color: $yellowColor;
                    border: 3px solid $yellowColor;

                    font-size: $FontSizeM;
                }
                button:hover{
                    background-color: $darkGreyColor;
                    border: 3px solid $darkGreyColor;
                    color: white; 
                }
                div.variant{
                    img{
                        height: 60px;
                    }
                    h2{
                        font-size: $FontSizeM;
                    }
                    p{
                        font-size: $FontSizeS;
                    }
                    h2,
                    p{
                        margin-top: 1rem;
                    }
                    width: 100%;
                }
            }
        }
    }
</style>