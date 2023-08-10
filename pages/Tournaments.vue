<script setup lang="ts">
interface TourInfo {
  title: string
  description: string
  image: string
  link: string
}

const cards = ref<TourInfo[]>([
  {
    title: 'Team A vs Team B',
    link: 'Watch on Twitch !',
    image: '/esport1.jpg',
    description: 'Front end development refers to the work that software developers do that is directly visible to the user.',
  },
  {
    title: 'Team A vs Team B',
    link: 'Watch on Twitch !',
    image: '/esport2.jpg',
    description: 'Front end development refers to the work that software developers do that is directly visible to the user.',
  },

])
</script>

<template>
  <h2 style="text-align:center" my6 text-4xl font-500>
    <p>Here you can see the upcomming tournaments</p>
  </h2>
  <p my1 mb-15 text-center text-6>
    Every tournament is streamed on
    <a href="" tag="a" class="ml1 block inline-block justify-center b-1px border-white rounded-2 bg-violet-800 px2 text-center transition-all-300 hover:bg-violet-900">twitch<svg class="float-right mt1 pl1" xmlns="http://www.w3.org/2000/svg" width="25" height="27" viewBox="0 0 24 24"><path fill="white" d="M11.571 4.714h1.715v5.143H11.57zm4.715 0H18v5.143h-1.714zM6 0L1.714 4.286v15.428h5.143V24l4.286-4.286h3.428L22.286 12V0zm14.571 11.143l-3.428 3.428h-3.429l-3 3v-3H6.857V1.714h13.714Z" /></svg></a>
  </p>
  <TournamentCardSection :cards="cards" />
</template>
