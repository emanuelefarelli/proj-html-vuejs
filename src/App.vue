<script>
import AppMain from './components/AppMain.vue'
import AppHeader from './components/AppHeader.vue'
import AppFooter from './components/AppFooter.vue'
export default{
  data(){
    return
  },
  components: {
    AppHeader,
    AppMain,
    AppFooter,
  }
}
</script>

<template>
  <AppHeader/>
  <AppMain/>
  <AppFooter/>
</template>

<style lang="scss">
  @use './styles/general.scss' as *;
</style>
