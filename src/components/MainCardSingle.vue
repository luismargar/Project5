<script setup>
import { faker } from '@faker-js/faker'
const fullname = faker.person.fullName()
const lastname = faker.person.lastName()


</script>

<template>
    {{ fullname }} <br />




</template>