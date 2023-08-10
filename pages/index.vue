<script setup lang="ts">
</script>

<template>
  <div class="flex flex-1 flex-col items-center justify-center">
    <h1 class="mt-4 flex flex-col text-center uppercase">
      <span class="color-transition-animation bg-gradient-to-r bg-clip-text text-5xl font-extrabold text-transparent lg:text-8xl">Random</span>
      <span class="color-transition-animation bg-gradient-to-r bg-clip-text text-5xl font-extrabold text-transparent lg:text-8xl">Legends</span>
      <span class="color-transition-animation bg-gradient-to-r bg-clip-text text-5xl font-extrabold text-transparent lg:text-8xl">Tournaments</span>
    </h1>
    <div class="mt-6 max-w-[500px] px-4 text-center md:max-w-[600px]">
      A place where you can play League of Legends tournaments, win rewards &amp; more.
    </div>
    <div class="ml-2 mt-8 flex justify-center space-x-4">
      <a
        href="" tag="a" class="h-14 flex cursor-pointer items-center justify-center border rounded-lg px-8 font-extrabold font-semibold text-white transition-all-300 duration-300 hover:bg-gray/7 focus:outline-none focus:ring-1 focus:ring-offset-1 focus:ring-gray-600/[0.6] focus:ring-offset-gray-800/[0.6] focus:dark:ring-gray-400 focus:dark:ring-offset-gray-50"
      >Sign up</a><a
        href="" tag="a" class="flex items-center b-1px border-white rounded-2 bg-black px3 text-center transition-all-300 hover:(bg-violet-900 text-white) focus:outline-none focus:ring-1 focus:ring-offset-1 focus:ring-gray-600/[0.6] focus:ring-offset-gray-800/[0.6] focus:dark:ring-gray-400 focus:dark:ring-offset-gray-50"
      >Watch on Twitch !<svg class="pl2 pt1" xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24"><path fill="#888888" d="M11.571 4.714h1.715v5.143H11.57zm4.715 0H18v5.143h-1.714zM6 0L1.714 4.286v15.428h5.143V24l4.286-4.286h3.428L22.286 12V0zm14.571 11.143l-3.428 3.428h-3.429l-3 3v-3H6.857V1.714h13.714Z" /></svg></a>
    </div>
  </div>
</template>

<style scoped>
.color-transition-animation {
  animation: colorTransitionLoop 10s infinite;
}

@keyframes colorTransitionLoop {
  0%, 100% {
    color: #FF5733; /* Start color */
  }
  10% {
    color: #33FF57; /* Transition to color 1 */
  }
  20% {
    color: #5733FF; /* Transition to color 2 */
  }
  30% {
    color: #d863f0; /* Transition back to start color */
  }
  40% {
    color: #65ebfd; /* Transition back to start color */
  }
  50% {
    color: #f8f521; /* Transition back to start color */
  }
  60% {
    color: #FF5733; /* Transition back to start color */
  }
  70% {
    color: #33FF57; /* Transition back to start color */
  }
  80% {
    color: #5733FF; /* Transition back to start color */
  }
  90% {
    color: #d863f0; /* Transition back to start color */
  }
  100% {
    color: #FF5733; /* Transition back to start color */
  }
}
</style>
