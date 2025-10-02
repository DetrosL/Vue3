<template>
  <TheHeader v-show="showHeader" />

  <div v-show="showName">
    Name: {{ firstName }} <br/>
    Last Name: {{ lastName }}
  </div>

  <div v-if="accessLevel === 'admin'">Admin</div>
  <div v-else-if="accessLevel === 'marketing'">Marketing</div>
  <div v-else>User</div>
</template>
<script setup>
import TheHeader from './components/TheHeader.vue'
import { ref } from 'vue'

const showHeader = ref(true)
const firstName = ref('Laiz')
const lastName = ref('Detros')
const showName = ref(false)
const accessLevel = ref('admin')
</script>
<style>
</style>
