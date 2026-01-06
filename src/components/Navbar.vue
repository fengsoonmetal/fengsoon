<template>
  <v-app-bar :elevation="2">
    <v-app-bar-title class="d-flex align-center ga-3">
      <router-link to="/" class="brand-link">
        <v-img
          :src="logo"
          alt="Feng Soon Logo"
          width="36"
          height="36"
          contain
          class="brand-logo"
        />
        <span class="text-h6 font-weight-bold">Feng Soon</span>
      </router-link>
    </v-app-bar-title>

    <v-spacer />

    <v-btn variant="text" to="/">Home</v-btn>
    <v-btn variant="text" to="/projects">Past Projects</v-btn>
    <v-btn variant="text" to="/about">About Us</v-btn>
    <v-btn variant="text" to="/contact">Contact Us</v-btn>
  </v-app-bar>
</template>

<script setup>
import logo from '@/assets/logo.png' // ✅ ensures Vite bundles it correctly
</script>

<style scoped>
/* remove "button feel" by using a normal link */
.brand-link {
  display: inline-flex;
  align-items: center;
  gap: 12px;
  text-decoration: none;
  color: inherit;
}

/* optional: keep logo crisp */
.brand-logo {
  flex: 0 0 auto;
}
</style>
