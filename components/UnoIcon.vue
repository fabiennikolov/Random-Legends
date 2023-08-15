<script setup lang="ts">
import type { UnoCssString } from '~/types'

defineProps<{
  icon: UnoCssString | string
}>()
</script>

<template>
  <i class="inline-block" :class="icon" />
</template>
