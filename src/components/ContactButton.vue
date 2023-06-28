<template>
    <div @click="this.itIsOpen = !this.itIsOpen" :class="(this.itIsOpen === false)? 'closed-contact':'open-contact'">
        <!-- QUANDO IL CONTATTO VIENE CHIUSO -->
        <div v-if="this.itIsOpen === false">
            <i class="fa-solid fa-phone"></i>
        </div>

        <!-- QUANDO IL CONTATTO VIENE APERTO -->
        <div v-else>
            <img src="https://freepngimg.com/save/22654-man/594x600" alt="Contact photo">
            <h2>
                John Smith
            </h2>
            <p>
                agent
            </p>
            <p>
                <i class="fa-solid fa-phone">+11211787</i>
            </p>
        </div>
    </div>
</template>
    
<script>
    export default{
        name: 'AppFooter',
        data(){
            return{
                itIsOpen: false,
            }
        },
    }
</script>
    
<style lang="scss" scoped>
    @use '../styles/partials/mixins.scss' as *;
    @use '../styles/partials/variables.scss' as *;
    div{
        @include flex();
        position: fixed;
        left: 15px;
        bottom: 30px;
        background-color: white;
        box-shadow: rgba(50, 50, 93, 0.25) 0px 13px 27px -5px, rgba(0, 0, 0, 0.3) 0px 8px 16px -8px;
    }
    div.closed-contact{
        div{
            width: 80px;
            height: 80px;
            border-radius: 50%;
            i.fa-phone{
                color: $yellowColor;
                font-size: $FontSizeL;
            }
        }
    }
    div.open-contact{
        div{
            @include flex( column);
            width: 300px;
            height: 250px;
            border-radius: 5px;
            img,
            h2,
            p{
                margin-bottom: 0.5rem;
            }
            img{
                height: 100px;
                width: 100px;
                border-radius: 50%;
            }
            h2{
                font-size: $FontSizeM;
            }
            p{
                font-size: $FontSizeS;
                
            }
        }
    }
</style>