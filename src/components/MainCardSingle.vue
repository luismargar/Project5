<script setup>
import { fa, faker } from '@faker-js/faker'
const fullname = faker.person.fullName()
const firstname = faker.person.firstName()
const lastname = faker.person.lastName()
const genre = faker.music.genre()
const bio = faker.lorem.lines(5)
const username = faker.internet.userName({firstName: firstname, lastName: lastname}).toLowerCase()


</script>

<template>
    <!-- {{ fullname }} <br /> -->
      <div class="border border-stone-600 rounded-xl shadow-lg bg-red-500">
        <img :src="faker.image.urlLoremFlickr({category: 'celebrity'})"/>
        <div class="p-5">
            <p class="mb-2 text-2xl font-bold">{{ fullname }}</p>
            <p class="mb-4 font-medium text-white">{{ genre }}</p>
            <p class="mb-4 font-medium text-white">{{ bio }}</p>
        </div>
      </div>




</template>