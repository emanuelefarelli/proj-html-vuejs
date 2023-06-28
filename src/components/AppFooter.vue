<template>
    <footer>
        <div class="container">
            <div>
                <img src="https://template186841.motopreview.com/mt-demo/186800/186841/mt-content/uploads/2021/06/mt-2236-home-logo.png" alt="Chess School logo">
                <p class="copyright">
                    Copyright © 2021. All Rights Reserved.
                </p>
            </div>
            <div>
                <h2>
                    Follow Us
                </h2>
                <nav class="brands">   
                    <a href="#">
                        <i class="fa-brands fa-facebook-f"></i>
                    </a>
                    <a href="#">
                        <i class="fa-brands fa-telegram"></i>
                    </a>
                    <a href="#">
                        <i class="fa-brands fa-instagram"></i>
                    </a>
                </nav>
            </div>
            <div class="email-input">
                <p>
                    Subscribe to get the latest news, course updates, discounts, events
                </p>
                <input type="text" placeholder="Enter your e-mail here*">
                <button>
                    Subscribe
                </button>
            </div>
        </div>
    </footer>
</template>
    
<script>
    export default{
        name: 'AppFooter',
        data(){
            return{
    
            }
        },
    }
</script>
    
<style lang="scss" scoped>
@use '../styles/partials/mixins.scss' as *;
@use '../styles/partials/variables.scss' as *;
    footer{
        height: 35vh;
        background-color: $darkerGreyColor;
        color: white;
        div.container{
            @include marginAuto;
            @include flex(row,space-between,flex-start);
            height: 100%;
            width: $dimension;
            div{
                margin-top: 4rem;
                p.copyright{
                    font-size: $FontSizeXS;
                    margin-top: 12rem;
                }
                h2{
                    font-size: $FontSizeML;
                    font-weight: 400;
                }
                nav.brands{
                    @include flex();
                    a{
                        color: white;
                        i.fa-brands{
                            @include flex();
                            width: 40px;
                            height: 40px;
                            margin-top: 2.5rem;
                            margin-right: 0.5rem;
                            font-size: $FontSizeXS;
                            border-radius: 4px;
                            border: 1px solid white;
                        }
                        i.fa-brands:hover{
                            color: $yellowColor;
                            border: 1px solid $yellowColor;

                        }
                    }
                }
            }
            div.email-input{
                @include flex(column,flex-start,flex-start);
                // width: 400px;
                p,
                input{
                    margin-bottom: 1rem;
                }
                p{
                    width: 450px;
                    font-size: $FontSizeS;
                }
                input{
                    width: 450px;
                    padding: 1rem;
                }
                button{
                    margin: 0;
                    background-color: $yellowColor;
                    font-size: $FontSizeM;
                }
                button:hover{
                    background-color: $darkGreyColor;
                    color: white;
                }
            }
        }
    }
</style>