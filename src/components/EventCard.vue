<template>
  <router-link :to="{ name: 'event-show', params: { id: event.id } }">
    <div class="rounded shadow p-8 mb-6 w-400px">
      <h3 class="mt-0 mb-2">
        {{ event.title }}
        <span class="font-normal">&bull; {{ event.date }}</span>
      </h3>
      <p class="text-grey-darker mt-0">{{ event.description }}</p>
      <div class="mb-6 mt-8 text-grey-darker flex items-center">
        <Zondicon icon="user-group" class="fill-current h-4 mr-2" />
        {{ event.attendees ? event.attendees.length : 0 }} attendees
      </div>
      <VMediaObject>
        <img
          :src="event.organizer.photo"
          :alt="`${event.organizer.name}'s photo`"
          slot="image"
          class="rounded-full h-10 inline-block"
        />
        <span slot="title" class="block">{{ event.organizer.name }}</span>
        <span slot="content" class="text-grey-darker">Status</span>
      </VMediaObject>
    </div>
  </router-link>
</template>

<script>
import Zondicon from 'vue-zondicons'

export default {
  props: { event: Object },
  components: {
    Zondicon
  }
}
</script>
