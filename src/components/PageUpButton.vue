<template>
        <div v-if="store.PageStart === false">
            <a href="#top">
                <i class="fa-solid fa-chevron-up"></i>
            </a>
        </div>
</template>
    
<script>
import {store} from '../store.js';
    export default{
        name: 'AppFooter',
        data(){
            return{
                store,
            }
        },
    }
</script>
    
<style lang="scss" scoped>
    @use '../styles/partials/mixins.scss' as *;
    @use '../styles/partials/variables.scss' as *;
    div{
        @include flex();
        width: 50px;
        height: 50px;
        position: fixed;
        bottom: 15px;
        right: 15px;
        border-radius: 50%;
        background-color: white;
        box-shadow: rgba(50, 50, 93, 0.25) 0px 13px 27px -5px, rgba(0, 0, 0, 0.3) 0px 8px 16px -8px;
        a{
            color: $yellowColor;
        }
    }
    .slide-fade-enter-active {
        transition: all 10s ease;
        transform: translateX(10px);
        opacity: 0;
    }
</style>