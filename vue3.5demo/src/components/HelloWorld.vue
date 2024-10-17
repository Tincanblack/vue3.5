<script setup>
import { ref, watch } from 'vue';

const innerCount = ref(0);

// const props = defineProps({
//   count: {
//     type: Number,
//     default: 0,
//   },
// });

// // error
// watch(props.count, (newVal) => {
//   innerCount.value = newVal;
// });

const { count = 0 } = defineProps({
  count: Number,
});

watch(
  () => count,
  (newVal) => {
    innerCount.value = newVal;
  }
);

// typescript
// const props = withDefaults(
//   defineProps<{
//     count: Number // type
//   }>(),
//   {
//     count: [] // 預設值
//   }
// );
</script>

<template>
  <p>Count: {{ count }}</p>
  <p>Inner count: {{ innerCount }}</p>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
