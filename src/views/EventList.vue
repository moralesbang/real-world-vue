<template>
  <router-link :to="{ name: 'event-show', params: { id: 12 } }">
    <div>
      <h1>Events Listing</h1>

      <EventCard />
    </div>
  </router-link>
</template>

<script>
import EventCard from '@/components/EventCard.vue'

export default {
  components: {
    EventCard
  }
}
</script>
