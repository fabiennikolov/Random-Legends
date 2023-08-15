<script setup lang="ts">

</script>

<template>
  <div class="relative isolate overflow-hidden py-16 text-sm lg:py-32 sm:py-24 lg:text-4">
    <div class="mx-auto max-w-6xl px-6 lg:px-6">
      <div class="grid grid-cols-1 mx-auto max-w-2xl gap-x-8 gap-y-16 lg:grid-cols-2 lg:max-w-none">
        <div class="max-w-xl lg:max-w-lg">
          <h2 class="text-center text-3xl font-bold tracking-tight text-white lg:text-start sm:text-4xl">
            Subscribe to our newsletter.
          </h2>
          <p class="mt-4 text-4 leading-7 text-gray-300">
            Stay informed about our latest news, events, and offers by subscribing to our newsletter. We'll deliver the most exciting updates right to your inbox.
          </p>
          <div class="mt-6 flex gap-x-4">
            <input id="email-address" name="email" type="email" autocomplete="email" required class="min-w-0 flex-auto border-0 rounded-md bg-white/9 px-3.5 py-2 text-white shadow-sm ring-1 ring-white/10 ring-inset sm:text-sm sm:leading-6" placeholder="Enter your email">
            <button type="submit" class="btn">
              Subscribe
            </button>
          </div>
        </div>
        <div class="flex gap-x-8 gap-y-10 sm:grid-cols-2 lg:pt-2">
          <div class="flex flex-col items-start">
            <div class="rounded-md bg-white/5 p-1 ring-1 ring-white/10">
              <UnoIcon icon="i-material-symbols-calendar-month-outline" h-8 w-8 />
            </div>
            <h1 class="mt-4 font-semibold text-white">
              Weekly articles
            </h1>
            <p class="mt-2 leading-7 text-gray-400">
              You will receive early access to our tournaments and events.
            </p>
          </div>
          <div class="flex flex-col items-start">
            <div class="rounded-md bg-white/5 p-1 ring-1 ring-white/10">
              <UnoIcon icon="i-heroicons:hand-raised" h-8 w-8 />
            </div>
            <h1 class="mt-4 font-semibold text-white">
              No spam
            </h1>
            <p class="mt-2 leading-7 text-gray-400">
              We wont send you useless stuff.
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
