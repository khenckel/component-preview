<template>
  <v-container class="d-flex justify-center align-center" style="height: 100vh;">
    <v-card width="600" height="400">
      <v-carousel>
        <v-carousel-item v-for="n in 5" :key="n">
          <v-container style="height: 100%;">
            <v-row justify="center" align="center" style="height: 100%;">
              <v-col cols="auto">
                <RandomComponent />
              </v-col>
            </v-row>
          </v-container>
        </v-carousel-item>
      </v-carousel>
    </v-card>
  </v-container>
</template>

<script setup>
import RandomComponent from './RandomComponent';
</script>
