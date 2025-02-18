<template>
  <v-btn :color="color" :variant="variant">Random Styled Button</v-btn>
</template>

<script setup>
import { ref } from 'vue';

// List of Vuetify color variants
const colors = [
  'primary', 'secondary', 'success', 'info', 'warning', 'error', 'dark', 'light'
];

// List of Vuetify button variants
const variants = [
  'contained', 'outlined', 'text'
];

// Function to get a random item from an array
const getRandomItem = (array) => {
  return array[Math.floor(Math.random() * array.length)];
};

const color = ref(getRandomItem(colors));
const variant = ref(getRandomItem(variants));
</script>
