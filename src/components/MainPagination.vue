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
<div class="flex justify-center gap-4 p-8">
    <button @click="prevPage" :disabled="activePage === 1" class="rounded-lg bg-orange-500 font-normal text-gray-700 shadow-md hover:bg-orange-800 hover:text-white">PREV</button>

    <button v-for="page in pages" :key="page" class="rounded-lg bg-orange-500 font-normal text-gray-700 shadow-md hover:bg-orange-800 hover:text-white" :class="page === activePage? 'bg-red-700 text-white': ''">{{ page }}</button>

    <button @click="nextPage" :disabled="activePage === pages" class="rounded-lg bg-orange-500 font-normal text-gray-700 shadow-md hover:bg-orange-800 hover:text-white">NEXT</button>
</div>





</template>