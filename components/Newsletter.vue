<script setup lang="ts">

</script>

<template>
  <div class="relative isolate overflow-hidden py-16 text-sm lg:py-32 sm:py-24 lg:text-4">
    <div class="mx-auto max-w-6xl px-6">
      <div class="grid grid-cols-1 mx-auto max-w-2xl gap-16 lg:grid-cols-2 lg:max-w-none">
        <div>
          <h2 class="text-center text-3xl font-bold tracking-tight text-white lg:text-start sm:text-4xl">
            Subscribe to our newsletter.
          </h2>
          <p class="mt-4 text-4 leading-7 text-gray-300">
            Stay informed about our latest news, events, and offers by subscribing to our newsletter. We'll deliver the most exciting updates right to your inbox.
          </p>
          <div class="mt-6 flex gap-x-4">
            <input id="email-address" name="email" type="email" autocomplete="email" required class="min-w-0 flex-auto border-0 rounded-md bg-white/9 px-3.5 py-2 text-white shadow-sm ring-1 ring-white/10 ring-inset sm:text-sm sm:leading-6" placeholder="Enter your email">
            <CoolButton>
              Subscribe
            </CoolButton>
          </div>
        </div>

        <div class="grid grid-cols-[repeat(auto-fill,_minmax(12rem,1fr))] gap-10">
          <HighlightItem icon="i-material-symbols-calendar-month-outline">
            <template #title>
              Weekly articles
            </template>
            <template #description>
              You will receive early access to our tournaments and events.
            </template>
          </HighlightItem>
          <HighlightItem icon="i-material-symbols-calendar-month-outline">
            <template #title>
              Weekly articles
            </template>
            <template #description>
              You will receive early access to our tournaments and events.
            </template>
          </HighlightItem>
          <HighlightItem icon="i-material-symbols-calendar-month-outline">
            <template #title>
              Weekly articles
            </template>
            <template #description>
              You will receive early access to our tournaments and events.
            </template>
          </HighlightItem>
          <HighlightItem icon="i-heroicons:hand-raised">
            <template #title>
              No spam
            </template>
            <template #description>
              We won't send you useless stuff.
            </template>
          </HighlightItem>
        </div>
      </div>
    </div>
  </div>
</template>
