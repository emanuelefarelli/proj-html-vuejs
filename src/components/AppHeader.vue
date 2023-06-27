<template>
    <header>
        <h1>Header</h1>
    </header>
</template>

<script>
    export default{
        name: 'AppHeader',
        data(){
            return{

            }
        },
    }
</script>

<style lang="scss" scoped>
    header{
        position: fixed;
        top: 1rem;
        z-index: 1;
    }
</style>