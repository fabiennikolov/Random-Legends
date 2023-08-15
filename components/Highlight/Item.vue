<script setup lang="ts">
import type { UnoCssString } from 'types'

defineProps<{
  icon?: UnoCssString
  title?: string
  description?: string
}>()
</script>

<template>
  <div class="flex flex-col">
    <div v-if="icon" class="aspect-square w-12 rounded-md bg-white/5 p-2 ring-1 ring-white/10">
      <UnoIcon :icon="icon" h-full w-full />
    </div>
    <h3 class="mt-4 font-semibold text-white">
      <slot name="title">
        {{ title }}
      </slot>
    </h3>
    <p class="mt-2 leading-7 text-gray-400">
      <slot name="description">
        {{ description }}
      </slot>
    </p>
  </div>
</template>
