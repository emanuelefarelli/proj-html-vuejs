<template>
    <header :class = "(this.PageStart === true)? '' : 'header-full'">

        <!-- PARTE SUPERIORE HEADER -->
        <div class="header-up" v-if="this.PageStart === true">
            <div>
                <i class="fa-solid fa-location-dot"></i>
                <span>
                    6767 Santa Monica Blvd,Los Angeles,CA 90038
                </span>
            </div>
            <div>
                <i class="fa-solid fa-phone"></i>
                <span>
                    Call Now <span>123-456-7890</span>
                </span>
                <button>
                        Donate
                </button>
            </div>
        </div>

        <!-- PARTE INFERIORE HEADER -->
        <div class="header-bottom">
            <div>
                <img src="https://template186841.motopreview.com/mt-demo/186800/186841/mt-content/uploads/2021/06/mt-2236-home-logo.png" alt="Chess School Logo">
            </div>
            <ul>
                <li v-for="link in NavLinks">
                    <a :href="link.link"> {{ link.title }} </a>
                </li>
            </ul>
        </div>
    </header>
</template>

<script>
import { store } from '../store.js';
    export default{
        name: 'AppHeader',
        data(){
            return{
                PageStart: true,
                NavLinks:[
                    {
                        title: 'Home',
                        link: '#'
                    },
                    {
                        title: 'Services',
                        link: '#'
                    },
                    {
                        title: 'Courses',
                        link: '#'
                    },
                    {
                        title: 'About',
                        link: '#'
                    },
                    {
                        title: 'FAQ',
                        link: '#'
                    },
                    {
                        title: 'Blog',
                        link: '#'
                    },
                    {
                        title: 'Contact Us',
                        link: '#'
                    },
                    store,
                ]
            }
        },
        methods: {

            // FUNZIONE PER VERIFICARE SE LA PAGINA E' ALL'INIZIO
            IsPageUp(){
                if(globalThis.scrollY <= 0){
                    store.PageStart = true;
                    this.PageStart = true;
                }else{
                    store.PageStart = false;
                    this.PageStart = false;
                };
            }
        },
        mounted(){
            globalThis.addEventListener("scroll", this.IsPageUp);
        }
    }
</script>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;
    header{
        width: 100%;
        position: fixed;
        z-index: 1;
        background-color: rgba(2, 0, 19, 0.39);
        color: white;
        div.header-up,
        div.header-bottom{
            width: $dimension;
            @include marginAuto;
            @include flex(row,space-between,center);
            height: 4.5rem;
        }

        div.header-up{
            span{
                font-size: $FontSizeS;
                margin-right: 6rem;
            }
            i{
                font-size: $FontSizeS;
                color: $yellowColor;
            }
            button{
                padding: 0.7rem 2.7rem;
                border: none;
                border-radius: 0.5rem;
                font-size: $FontSizeS;
                font-weight: 600;
            }
            button:hover{
                background-color: $yellowColor;
            }
        }
        div.header-bottom{
            ul{
                @include flex();
                li{
                    margin-right: 1.5rem;
                    a{
                        color: white;
                    }
                    a:hover{
                        color: $yellowColor;
                    }
                }
            }
        }
    }
    header.header-full{
        background-color: rgba(2, 0, 19);
    }
</style>