<script setup>
import EventCard from '@/components/EventCard.vue'
import { ref } from 'vue'

const events = ref([
  {
    id: 5928101,
    category: 'animal welfare',
    title: 'cat adoption day',
    description: 'find your new feline friend at this event.',
    location: 'Meow Town',
    date: 'January 28, 2022',
    time: '12:00',
    petsAllowed: true,
    organizer: 'Kat Laydee',
  },
  {
    id: 5928102,
    category: 'environment',
    title: 'tree planting drive',
    description: 'join us to plant trees and make the planet greener.',
    location: 'Green Park',
    date: 'February 15, 2022',
    time: '10:00',
    petsAllowed: false,
    organizer: 'Eco Warriors',
  },
  {
    id: 5928103,
    category: 'education',
    title: 'coding bootcamp',
    description: 'learn the basics of web development in this workshop.',
    location: 'Tech Hub',
    date: 'March 10, 2022',
    time: '09:00',
    petsAllowed: false,
    organizer: 'Code Masters',
  },
  {
    id: 5928104,
    category: 'health',
    title: 'yoga session',
    description: 'relax and rejuvenate with a guided yoga session.',
    location: 'Wellness Center',
    date: 'April 5, 2022',
    time: '07:00',
    petsAllowed: true,
    organizer: 'Zen Life',
  },
  {
    id: 5928105,
    category: 'community',
    title: 'neighborhood cleanup',
    description: 'help us clean up and beautify our neighborhood.',
    location: 'Main Street',
    date: 'May 20, 2022',
    time: '08:00',
    petsAllowed: true,
    organizer: 'Community Helpers',
  },
  {
    id: 5928106,
    category: 'arts',
    title: 'painting workshop',
    description: 'unleash your creativity in this fun painting workshop.',
    location: 'Art Studio',
    date: 'June 12, 2022',
    time: '14:00',
    petsAllowed: false,
    organizer: 'Creative Minds',
  },
])
</script>

<template>
  <h1>Events For Good</h1>

  <div class="events">
    <EventCard v-for="event in events" :key="event.id" :event="event" />
  </div>
</template>

<style scoped>
.events {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
