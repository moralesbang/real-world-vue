<template>
  <div id="app" class="text-base">
    <Navbar />
    <router-view class="flex justify-center mb-10 this-is-the-router-view" />
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
