<script setup lang="ts">
const router = useRouter()
</script>

<template>
  <main p="x4 y10" text="center dark:gray-200">
    <h1 text-6 font-bold>
      404
    </h1>
    <div text-4xl>
      <div i-carbon-warning inline-block />
    </div>
    <div>Page Not found</div>
    <div>
      <button text-sm btn m="3 t8" @click="router.back()">
        Back
      </button>
    </div>
  </main>
</template>
