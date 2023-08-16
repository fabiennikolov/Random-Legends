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
    <a href="https://www.twitch.tv/" target="_blank">
      <CoolButton class="ml2" bg="#6441A4" border-violet-6 text-white hover="border-white"> Twitch
        <UnoIcon icon="i-mdi-twitch" ml1 />
      </CoolButton>
    </a>
  </p>
  <TournamentCardSection :cards="cards" />
  <Newsletter />
</template>
