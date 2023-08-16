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
      >Sign up</a>
      <CoolButton intent="unstyled" bg-violet-6 border-violet-6 text-white hover="border-white">
        Watch on Twitch !
        <UnoIcon icon="i-mdi-twitch" class="ml1 w8 h8" />
      </CoolButton>
    </div>
  </div>
  <div class="mx-auto mt-10 max-w-300 px-15 py-10 leading-6 space-y-14">
    <section class="grid gap-10 md:grid-cols-[1.5fr_1fr]">
      <div lt-md="text-center" text-end="">
        <h3 uppercase="" text-2xl="" mb-4="" font-bold="">
          Unique Gameplay Experience
        </h3>
        <p lt-md:text-3.5>
          This custom game mode offers a unique twist to the traditional League of Legends experience. The randomization element adds an element of surprise and challenge, making each game different and exciting.
        </p>
      </div>
      <img src="/esport1.jpg" width="400" lt-md="justify-self-center" rounded-2>
    </section>
    <section class="grid gap-10 md:grid-cols-[1fr_1.5fr]">
      <img src="/esport2.jpg" width="400" lt-md="justify-self-center" rounded-2>
      <div lt-md="text-center" text-start="">
        <h3 uppercase="" text-2xl="" mb-4="" font-bold="">
          Appeal to Variety Seekers
        </h3>
        <p lt-md:text-3.5>
          Players who enjoy diverse gameplay experiences and thrive on adapting to new situations are the perfect match for this custom game mode. The random champion selection and itemization will require players to think on their feet, adapt their strategies, and make the most out of the resources they have.
        </p>
      </div>
    </section>
  </div>
  <Newsletter />
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
    color: #d863f0;
  }
  40% {
    color: #65ebfd;
  }
  50% {
    color: #f8f521;
  }
  60% {
    color: #FF5733;
  }
  70% {
    color: #33FF57;
  }
  80% {
    color: #5733FF;
  }
  90% {
    color: #d863f0;
  }
  100% {
    color: #FF5733;
  }
}
</style>
