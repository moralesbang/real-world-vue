<template>
  <div id="app" class="text-base">
    <Navbar />
    <router-view />
  </div>
</template>

<script>
import Navbar from '@/components/Navbar.vue'

export default {
  components: {
    Navbar
  }
}
</script>

<style lang="sass">
body
  padding: 0
  margin: 0
</style>
