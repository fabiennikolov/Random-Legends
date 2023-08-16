<script setup lang="ts">
import type { SocialLink } from 'types'

const menuItems = [
  { id: 1, text: 'FAQ', route: '/faq' },
  { id: 2, text: 'Register a team', route: '/contacts' },
  { id: 3, text: 'Upcoming tournaments', route: '/tournaments' },
  { id: 4, text: 'Become a partner', route: '/partner' },
  { id: 5, text: 'Rules', route: '/rules' },
]

const socialLinks: SocialLink[] = [

]
</script>

<template>
  <footer class="border-t-1 b-white/9 py-2 text-white/80">
    <div class="mx-auto max-w-6xl flex flex-1 flex-col items-center justify-between px-4 py-2 text-center text-xs text-gray-400 md:flex-row space-y-2 md:text-left md:space-y-0">
      <div>
        Copyright © 2023 Random Legends. All rights reserved. Random Legends isn't endorsed by Riot Games and doesn't reflect the views or opinions of Riot Games or anyone officially involved in producing or managing Riot Games properties. Riot Games, and all associated properties are trademarks or registered trademarks of Riot Games, Inc.
      </div>
      <div flex flex-col items-end>
        <ul>
          <li flex gap-2>
            <a href="">
              <UnoIcon class="w8 h8" icon="i-ic-round-facebook" />
            </a>
            <a href="">
              <UnoIcon class="w8 h8" icon="i-mdi-instagram" />
            </a>
            <a href="https://www.tiktok.com/@fab_league" target="_blank">
              <UnoIcon class="w8 h8" icon="i-ic-round-tiktok" />
            </a>
            <a href="https://discord.gg/3x9EVjfUjC" target="_blank">
              <UnoIcon class="w8 h8" icon="i-ic-baseline-discord" />
            </a>
            <a href="">
              <UnoIcon class="w8 h8" icon="i-mdi-twitch" />
            </a>
          </li>
        </ul>
      </div>
    </div>
    <div class="mx-auto max-w-1120px flex items-center justify-center px-4 py-2 text-center text-gray-400 md:flex-row lg:text-5">
      <section>
        <ul flex gap-5 lg:py-5 uppercase>
          <li>
            <NuxtLink to="/">
              Home
            </NuxtLink>
          </li>
          <li>
            <NuxtLink to="/faq">
              Faq
            </NuxtLink>
          </li>
          <li>
            <NuxtLink to="/rules">
              Rules
            </NuxtLink>
          </li>
        </ul>
      </section>
    </div>
  </footer>
</template>
