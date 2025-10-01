<template>
  <TheHeader 
    v-show="showHeader"
  /><!-- ou <TheHeader></TheHeader> -->
  
  <div v-show="showName">
    Name: {{ fistName }} <br/>
    Last Name: {{ lastName }}
  </div>

  <div v-if="accessLevel === 'admin'">Admin</div>
  <div v-else-if="accessLevel === 'marketing'">Marketing</div>
  <div v-else>User</div>

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
        fistName: 'Laiz',
        lastName: 'Detros',
        showName: false,
        accessLevel: 'admin'
      }
    }
  }
</script>

<style>
  
</style>
