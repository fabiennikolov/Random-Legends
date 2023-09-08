<script setup lang="ts">
interface TourInfo {
  title: string
  description: string
  image: string
  link: string
}

defineProps<{
  cards: TourInfo[]
}>()
</script>

<template>
  <div class="grid mx-auto max-w-6xl justify-center gap-6 p-4 lg:grid-cols-4 lt-lg:w-fit">
    <TournamentCard
      v-for="card in cards" :key="card.title"
      v-bind="card"
    />
  </div>
</template>
