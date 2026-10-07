<script setup>
const photo = "https://i.pinimg.com/1200x/ad/7e/a8/ad7ea8fe1a805644f23c0436e3224f2a.jpg"
const btn = false;
</script>


<template>

<div>
    <!-- <img v-bind:src= "photo" alt="Ma photo"> -->
<img :src= "photo" alt="Ma photo">
<button :disabled="btn">Click Me</button>
</div>

</template>


<style scoped>


</style>