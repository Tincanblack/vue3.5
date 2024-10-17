<script setup>
import { ref, useTemplateRef } from "vue";

const inputElement = ref(null);

const focus = () => {
    inputElement.value.focus();
}


// 3.5
// const inputRef = useTemplateRef('inputElement');
// const focus = () => {
//     inputRef.value.focus();
// }

const count = ref(0);
</script>

<template>
  <div>
    <input type="text" ref="inputElement">
    <div>
      <button @click="focus">input focus</button>
    </div>
  </div>
</template>

<style scoped>
</style>
