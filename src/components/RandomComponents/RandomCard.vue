<template>
  <v-card :color="color" class="pa-5">
    <v-card-title>Random Styled Card</v-card-title>
    <v-card-text>This is a randomly styled card.</v-card-text>
  </v-card>
</template>

<script setup>
import { ref } from 'vue';

// List of Vuetify color variants
const colors = [
  'primary', 'secondary', 'success', 'info', 'warning', 'error', 'dark', 'light'
];

// Function to get a random item from an array
const getRandomItem = (array) => {
  return array[Math.floor(Math.random() * array.length)];
};

const color = ref(getRandomItem(colors));
</script>
