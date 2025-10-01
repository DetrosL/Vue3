<template>
  <TheHeader 
    v-show="showHeader"
  />
  
</template>
<script>
  import TheHeader from './components/TheHeader.vue'

  export default {
    name: 'App',
    components: {
      TheHeader
    },
    data(){
      return {
        showHeader: true,
      }
    }
  }
</script>
<style>
  
</style>
