<template>
    <main>
        <PageUpButton/>
        <AppJumbotron/>
        <AppServices/>
        <AppPhotobook/>
        <AppCourses/>
        <AppFirstStep/>
        <AppEvents/>
        <AppNews/>
        <AppFooter/>
    </main>
</template>
    
<script>
    import PageUpButton from './PageUpButton.vue';
    import AppJumbotron from './AppJumbotron.vue';
    import AppServices from './AppServices.vue';
    import AppPhotobook from './AppPhotobook.vue';
    import AppCourses from './AppCourses.vue';
    import AppFirstStep from './AppFirstStep.vue';
    import AppEvents from './AppEvents.vue'
    import AppNews from './AppNews.vue'
    import AppFooter from './AppFooter.vue';

    export default{
        name: 'AppMain',
        data(){
            return{
            }
        },
        components: {
            PageUpButton,
            AppJumbotron,
            AppServices,
            AppPhotobook,
            AppCourses,
            AppFirstStep,
            AppEvents,
            AppNews,
            AppFooter
        },
        
        methods: {
        }
    }

</script>
    
<style lang="scss" scoped>
    
</style>