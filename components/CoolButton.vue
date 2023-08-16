<script setup lang="ts">
import { cva } from 'class-variance-authority'

withDefaults(defineProps<{
  intent?: 'primary' | 'accent' | 'unstyled'
  overlayClass?: string
}>(), {
  intent: 'primary',
})

const buttonClass = computed(() => {
  return cva(
    'text-white border-white',
    {
      variants: {
        intent: {
          primary: '',
          accent: '',
        },
      },
    })
})
</script>

<template>
  <button
    type="submit" class="group relative isolate overflow-hidden btn"
    :class="{ ' text-white border-1 border-white': intent !== 'unstyled' }"
  >
    <div
      class="absolute -top-4 -bottom-4 -left-10 -right-10 -z-1"
      :class="[{ 'bg-white text-[#222222]': !overlayClass }, overlayClass]"
      rounded="50%"
      transition-all-500 translate-y="100%" group-hover="translate-y-0"
      flex items-center justify-center
    >
      <slot />
    </div>
    <span class="invisible">
      <slot />
    </span>
    <span
      absolute inset-0
      transition-all-500 group-hover="-translate-y-50% opacity-0"
      flex items-center justify-center
    >
      <slot />
    </span>
  </button>
</template>
