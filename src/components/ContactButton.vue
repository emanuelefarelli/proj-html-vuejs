<template>
    <div>
        <i class="fa-solid fa-phone"></i>
    </div>
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
    div{
        @include flex();
        width: 80px;
        height: 80px;
        position: fixed;
        bottom: 30px;
        left: 15px;
        border-radius: 50%;
        background-color: white;
        box-shadow: rgba(50, 50, 93, 0.25) 0px 13px 27px -5px, rgba(0, 0, 0, 0.3) 0px 8px 16px -8px;
        i{
            color: $yellowColor;
            font-size: $FontSizeL;
        }
    }
</style>