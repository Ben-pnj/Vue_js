<script setup>
import { ref, watch } from 'vue'
const msg = ref('Hello de composants')
</script>

<template>
    <h1>{{ msg }}</h1>
</template>



<style scoped>

h1{
    color: blueviolet;
}

</style>