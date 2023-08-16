<script setup lang="ts">
interface TourInfo {
  title: string
  description: string
  image: string
  link: string
}

defineProps<TourInfo>()
</script>

<template>
  <div
    b="1 transparent" class="max-w-75 w-full overflow-hidden b-1px b-white/20 rounded-3 p-4 shadow-xl drop-shadow-xl space-y-6 hover:bg-gray/7 sm:p-8"
  >
    <h4 class="text-(center 2xl) font-(extrabold) leading-relaxed">
      {{ title }}
    </h4>
    <div flex="~ col" class="items-center gap-3">
      <div class="h-40 w-50">
        <img :src="image" class="mx-auto h-full object-contain">
      </div>
      <CoolButton>
        <a
          :href="link" target="_blank"
        >
          {{ link }}
        </a>
      </CoolButton>
    </div>
    <p v-if="description" class="mt-10px text-center leading-7">
      {{ description }}
    </p>
  </div>
</template>
