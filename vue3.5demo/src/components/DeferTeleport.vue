<script setup>

</script>

<template>

    <div id="container1"></div>
    <teleport to='#container1'>
        <div>Teleport to container1</div>
    </teleport>
    <!-- 3.5 -->
    <teleport defer to='#container2'>
        <div>Teleport to container2</div>
    </teleport>
    <div id="container2"></div>
</template>

<style scoped>
</style>
