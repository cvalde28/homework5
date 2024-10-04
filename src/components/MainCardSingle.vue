<script setup>
import { faker } from '@faker-js/faker';
const fullname = faker.person.fullname()
const firstname = faker.person.firstname()
const lastname = faker.person.lastname()
const job_title = faker.person.job_title()
const bio = faker.person.lines(2)
const username = faker.person.username({firstName: firstname, lastname:lastName}).toLowerCase()

</script>

<template>
    <!-- {{ fullname }} <br /> -->
      <div class="border border-gray-400 rounded-lg shadow bg-gray-200 h-full">
        <img :src="faker.image.urlLoremFlicker({category: 'cat'})" class="rounded-t-xl" />
      <div class="p-4">
        <p class="mb-2 text-2xl font-bold">{{ fullname }}</p>
        <p class="mb-3 font-normal text-gray-700">{{ job_title }}</p>
        <p class="mb-3 font-normal text-gray-700">{{ bio }}</p>
    </div>
    </div>
</template>