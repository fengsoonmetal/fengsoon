<template>
  <v-footer
    class="d-flex align-center justify-center ga-2 flex-wrap flex-grow-1 py-3"
    color="surface-light"
  >
    <v-btn
      v-for="link in links"
      :key="link.text"
      :to="link.to"
      variant="text"
      rounded
    >
      {{ link.text }}
    </v-btn>

    <div class="flex-1-0-100 text-center mt-2">
      {{ new Date().getFullYear() }} — <strong>Feng Soon</strong>
    </div>
  </v-footer>
</template>

<script setup>
const links = [
  { text: 'Home', to: '/' },
  { text: 'Past Projects', to: '/projects' },
  { text: 'About Us', to: '/about' },
  { text: 'Contact Us', to: '/contact' },
]
</script>
