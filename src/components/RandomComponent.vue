<template>
  <component :is="randomComponent" />
</template>

<script setup>
import { ref, watchEffect } from 'vue';
import RandomButton from './RandomComponents/RandomButton.vue';
import RandomCard from './RandomComponents/RandomCard.vue';
import RandomChip from './RandomComponents/RandomChip.vue';

// List of components to randomly select from
const components = [RandomButton, RandomCard, RandomChip];

// Function to get a random item from an array
const getRandomItem = (array) => {
  return array[Math.floor(Math.random() * array.length)];
};

const randomComponent = ref(getRandomItem(components));

// Watch effect to update the random component each time it is rendered
watchEffect(() => {
  randomComponent.value = getRandomItem(components);
});
</script>
