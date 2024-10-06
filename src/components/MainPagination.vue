<script setup>
import { ref } from 'vue'
const pages = ref(10)
const activePage = ref(1)

const prevPage = () => {
    if (activePage.value > 1) {
        activePage.value--
    }

    console.log(activePage.value)
}

const nextPage = () => {
    if (activePage.value < pages.value) {
        activePage.value++
    }

    console.log(activePage)
}

console.log(activePage.value)

</script>

<template>
<div>
    <button @click="prevPage" :disabled="activePage === 1">PREV</button>
    <button v-for="page in pages" :key="page" class="">{{ page }}</button>
    <button @click="nextPage" :disabled="activePage === pages">NEXT</button>
</div>





</template>