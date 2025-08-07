<script setup lang="ts">
import { ref } from 'vue'

const title = ref('Dashboard')
</script>

<template>
  <v-container fluid>
    <v-row>
      <v-col cols="12">
        <v-card>
          <v-card-title class="text-h4">
            {{ title }}
          </v-card-title>
          <v-card-text>
            <p class="text-body-1">Bienvenue sur le Dashboard de Veezit Admin.</p>
            <p class="text-body-2 text-medium-emphasis">
              Cette page est un placeholder pour le dashboard principal.
            </p>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>
