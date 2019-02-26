<template>
  <div class="bg-grey-darkest text-white py-4 mb-10 flex justify-center">
    <div class="container flex items-center justify-around">
      <router-link to="/" class="flex items-center">
        <Zondicon icon="bolt" class="fill-current h-5 mr-2" />
        <span class="font-semibold text-xl">Real World Events</span>
      </router-link>

      <nav class="inline-block">
        <router-link :to="{ name: 'event-list' }" class="btn">List</router-link>
        <router-link :to="{ name: 'event-create' }">
          <button type="button" class="btn btn-primary">Create</button>
        </router-link>
      </nav>
    </div>
  </div>
</template>

<script>
import Zondicon from 'vue-zondicons'

export default {
  components: {
    Zondicon
  }
}
</script>

<style lang="sass" scoped>
nav
  a
    font-weight: bold
  a:not(:last-child)
    margin-right: 1em
</style>
