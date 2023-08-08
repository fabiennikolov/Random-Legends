<template>
  <div class="mx-auto max-w-screen-2xl flex flex-1 items-center justify-between px-4">
    <div class="flex justify-center gap-8 lg:text-1rem">
      <NuxtLink to="/">
        <img src="@/logo.png" class="my3 inline-block max-w-45">
      </NuxtLink>
    </div>
    <div class="flex items-center justify-between text-sm text-white/80 space-x-4">
      <NuxtLink to="/">
        FAQ
      </NuxtLink>
      <NuxtLink to="/contacts">
        Contacts
      </NuxtLink>
      <button class="b-1px border-white/30 rounded-2 bg-black px3 hover:(bg-violet-900 text-white)">
        <NuxtLink to="/" class="mt3 flex">
          Watch on Twitch !
          <svg class="pb2 pl3" xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24"><path fill="#888888" d="M11.571 4.714h1.715v5.143H11.57zm4.715 0H18v5.143h-1.714zM6 0L1.714 4.286v15.428h5.143V24l4.286-4.286h3.428L22.286 12V0zm14.571 11.143l-3.428 3.428h-3.429l-3 3v-3H6.857V1.714h13.714Z" /></svg>
        </NuxtLink>
      </button>
    </div>
  </div>
</template>

<style scoped>
a:hover {
  color: white;
}
</style>
