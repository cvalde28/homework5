<script setup>
import MainCardSingle from './MainCardSingle.vue';

const cardCount = Array.from({ length: 20 }); // Creates an array with 20 undefined elements
</script>

<template>
<div class="grid grid-cols-5 gap-10 p-10">
    <MainCardSingle v-for="(card, index) in cardCount" :key="index"></MainCardSingle>
</div>


</template>
