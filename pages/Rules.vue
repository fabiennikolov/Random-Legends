<template>
  <h1 class="mt-10 text-center lg:text-6 md:text-5 font-600">
    The rules are available in
    <a href="https://www.twitch.tv/" target="_blank">
      <CoolButton class="ml2" bg="#7289da" text-white hover="border-white"> Discord
        <UnoIcon icon="i-ic-baseline-discord" ml1 />
      </CoolButton>
    </a>
  </h1>
  <div class="grid mx-auto max-w-6xl justify-center gap-6 p-4 lg:grid-cols-4 lt-lg:w-fit mt15 ">
    <div class="max-w-75 w-full overflow-hidden b-1px b-white/20 rounded-3 p-4 shadow-xl drop-shadow-xl space-y-6 hover:bg-gray/7 sm:p-8">
      asdasd
    </div>
    <div class="max-w-75 w-full overflow-hidden b-1px b-white/20 rounded-3 p-4 shadow-xl drop-shadow-xl space-y-6 hover:bg-gray/7 sm:p-8">
      asdasd
    </div>
  </div>
  <div class="grid mx-auto max-w-6xl justify-center gap-6 p-4 lg:grid-cols-4 lt-lg:w-fit mt15">
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
</template>
