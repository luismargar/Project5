<script setup>
import { fa, faker } from '@faker-js/faker'
import { RouterLink } from 'vue-router'
const firstname = faker.person.firstName()
const lastname = faker.person.lastName()
const fullname = faker.person.fullName({firstName: firstname, lastName: lastname})
const genre = faker.music.genre()
const date = faker.date.future()
const bio = faker.lorem.lines(5)
const username = faker.internet.userName({firstName: firstname, lastName: lastname}).toLowerCase()


</script>

<template>
    <!-- {{ fullname }} <br /> -->
      <RouterLink :to="{ name: 'CardDetails', params: { id: username}}">
      <div class="border border-stone-600 rounded-xl shadow-lg bg-red-500">
        <img :src="faker.image.urlLoremFlickr({category: 'celebrity'})" class="rounded-t-xl" height="300" width="300"/>
        <div class="p-5">
            <p class="mb-2 text-2xl font-bold">{{ fullname }}</p>
            <p class="mb-4 font-medium text-white">{{ genre }}</p>
            <p class="mb-4 font-medium text-white">{{ date }}</p>
            <p class="mb-4 font-medium text-white">{{ bio }}</p>
        </div>
      </div>
      </RouterLink>



</template>