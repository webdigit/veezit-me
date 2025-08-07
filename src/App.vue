<script setup lang="ts">
import { ref, computed } from 'vue'
import { RouterView, useRoute } from 'vue-router'

const route = useRoute()
const drawer = ref(true)
const rail = ref(false)

const toggleDrawer = () => {
  drawer.value = !drawer.value
}

// Vérifier si on est sur la page de login
const isLoginPage = computed(() => route.name === 'login')
</script>

<template>
  <v-app>
    <!-- Layout principal seulement si pas sur la page de login -->
    <template v-if="!isLoginPage">
      <!-- App Bar -->
      <v-app-bar color="primary" prominent>
        <v-app-bar-nav-icon @click="toggleDrawer" />
        <v-app-bar-title>Veezit Admin</v-app-bar-title>
        <v-spacer />
        <v-btn icon="mdi-account" />
      </v-app-bar>

      <!-- Navigation Drawer -->
      <v-navigation-drawer v-model="drawer" :rail="rail" permanent @click="rail = false">
        <v-list-item
          prepend-avatar="https://randomuser.me/api/portraits/men/85.jpg"
          :title="rail ? '' : 'John Doe'"
          nav
        >
          <template v-slot:append>
            <v-btn variant="text" icon="mdi-chevron-left" @click.stop="rail = !rail" />
          </template>
        </v-list-item>

        <v-divider />

        <v-list density="compact" nav>
          <v-list-item prepend-icon="mdi-view-dashboard" title="Dashboard" value="dashboard" to="/" />
          <v-list-item prepend-icon="mdi-login" title="Connexion" value="login" to="/login" />
        </v-list>
      </v-navigation-drawer>

      <!-- Main Content -->
      <v-main>
        <v-container fluid>
          <RouterView />
        </v-container>
      </v-main>
    </template>

    <!-- Page de login sans layout principal -->
    <template v-else>
      <RouterView />
    </template>
  </v-app>
</template>

<style scoped>
.v-main {
  background-color: #f5f5f5;
}
</style>
