<script setup>
import { ref, watch, onWatcherCleanup } from "vue";

const count = ref(0);
watch(count, () => {
    const timer = setTimeout(() => {
      console.log('現在數到,', count.value);
    }, 2000);
    
    // onWatcherCleanup(() => {
    //     clearTimeout(timer);
    // });
});


</script>

<template>
  <div>
    <div>
      <button @click="count++">count+1</button>
    </div>
  </div>
</template>

<style scoped>
</style>
