<template>
    <header>
        <div class="header-up" v-if="this.PageStart === true">
            <h1>header</h1>
        </div>
        <div class="header-bottom">
            <h1>header</h1>
        </div>
    </header>
</template>

<script>
    export default{
        name: 'AppHeader',
        data(){
            return{
                PageStart: true
            }
        },
        methods: {
            IsPageUp(){
                console.log(globalThis.scrollY);
                if(globalThis.scrollY <= 0){
                    this.PageStart = true;
                }else{this.PageStart = false};
            }
        },
        mounted(){
            globalThis.addEventListener("scroll", this.IsPageUp)
        }
    }
</script>

<style lang="scss" scoped>
    header{
        position: fixed;
        z-index: 1;
    }
</style>