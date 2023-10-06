<script setup lang="ts">
const showMobileMenu = ref(false)

const menuItems = [
  { text: 'FAQ', route: '/faq' },
  { text: 'Register a team', route: '/contacts' },
  { text: 'Upcoming tournaments', route: '/tournaments' },
  { text: 'Become a partner', route: '/partner' },
  { text: 'Rules', route: '/rules' },
]

function toggleMobileMenu() {
  showMobileMenu.value = !showMobileMenu.value
}
</script>

<template>
  <div class="sticky top-0 z-100 nav-container backdrop-blur bg-transparent">
    <div class="mx-auto w-full flex items-center justify-between border-b-1 border-white/9 px-4">
      <div class="flex justify-center gap-8 lg:text-1rem">
        <NuxtLink to="/">
          <img src="@/logo.png" class="my-3 inline-block max-w-35 lg:max-w-45">
        </NuxtLink>
        <Search />
      </div>
      <div class="flex items-center justify-between uppercase space-x-4">
        <button class="text-white lg:hidden" @click="toggleMobileMenu">
          <UnoIcon icon="i-iconamoon-menu-burger-horizontal" w8 h8 />
        </button>
        <div class="hidden text-sm font-600 text-white/80 lg:flex space-x-4">
          <template v-for="item in menuItems" :key="item.id">
            <NuxtLink :to="item.route" class="px2 py2 hover:(rounded-md bg-white/9)" @click="toggleMobileMenu">
              {{ item.text }}
            </NuxtLink>
          </template>
        </div>
      </div>
    </div>
    <transition name="fade">
      <div v-if="showMobileMenu" class="grid border-b-1 b-white/9 p-4 text-center lg:hidden space-y-2">
        <template v-for="item in menuItems" :key="item.id">
          <NuxtLink :to="item.route" class="text-white/80 hover:(rounded-3 bg-white/9)" @click="toggleMobileMenu">
            {{ item.text }}
          </NuxtLink>
        </template>
      </div>
    </transition>
  </div>
</template>

<style scoped>
a:hover {
  color: white;
}

.fade-enter-active, .fade-leave-active {
  transition: opacity 0.5s;
}

.fade-enter, .fade-leave-to {
  opacity: 0;
}
</style>
