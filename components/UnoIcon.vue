<script setup lang="ts">
import type { UnoCssString } from '~/types'

defineProps<{
  icon: UnoCssString | string
}>()
</script>

<template>
  <i class="inline-block h8 w8" :class="icon" />
</template>
