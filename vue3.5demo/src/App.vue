<script setup>
import { ref } from "vue";
import HelloWorld from './components/HelloWorld.vue'
import TemplateRef from './components/TemplateRef.vue'
import DeferTeleport from './components/DeferTeleport.vue'
import OnWatcherCleanUp from './components/OnWatcherCleanUp.vue'

const count = ref(0);
</script>

<template>
  <!-- props -->
  <HelloWorld :count />
  <button @click="count++">+1</button>

  <!-- useTemplateRef -->
  <TemplateRef />

  <!-- deferTemplate -->
  <DeferTeleport /> 

  <!-- onWatcherCleanUp -->
   <OnWatcherCleanUp />

</template>

<style scoped>
</style>
