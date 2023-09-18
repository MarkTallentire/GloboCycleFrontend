<template>
  <q-page class='row items-start justify-evenly'>
    <EventCard :events="events" />
  </q-page>
</template>

<script setup lang='ts'>
import { Event } from 'components/models';
import { ref } from 'vue';
import EventCard from '../components/EventCard.vue'

const events = ref<Event[]>([
  {
    id: 1,
    type: 'Audax',
    name: 'Audax 2022',
    body: '200 miles across hilly terrain in the North East, you in?',
    time: '12/03/2024, 6AM'
  },
  {
    id: 2,
    type: 'Audax',
    name: 'Audax 2022',
    body: '200 miles across hilly terrain in the North East, you in?',
    time: '12/03/2024, 6AM'

  },
  {
    id: 3,
    type: 'Audax',
    name: 'Audax 2022',
    body: '200 miles across hilly terrain in the North East, you in?',
    time: '12/03/2024, 6AM'

  }
]);

</script>
