<template>
  <TheHeader v-show="showHeader" />
</template>
<script setup>
    import { ref } from 'vue'
    import TheHeader from './components/TheHeaderV.vue'

    const showHeader = ref(true)
</script>
<style>
</style>
