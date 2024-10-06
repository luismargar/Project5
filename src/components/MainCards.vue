<script setup>
import MainCardSingle from './MainCardSingle.vue';
</script>


<template>
<MainCardSingle v-for="card in 20" :key="card"></MainCardSingle>


</template>