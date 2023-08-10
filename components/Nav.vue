<script setup lang="ts">
const showMobileMenu = ref(false)

function toggleMobileMenu() {
  showMobileMenu.value = !showMobileMenu.value
}
</script>

<template>
  <div class="nav-container">
    <div class="mx-auto max-w-screen-2xl flex items-center justify-between border-b-1 border-white/9 px-4">
      <div class="flex justify-center gap-8 lg:text-1rem">
        <NuxtLink to="/">
          <img src="@/logo.png" class="my-3 inline-block max-w-45">
        </NuxtLink>
      </div>
      <div class="flex items-center justify-between space-x-4">
        <button class="text-white lg:hidden" @click="toggleMobileMenu">
          <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24"><path fill="none" stroke="#888888" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 6.001h18m-18 6h18m-18 6h18" /></svg>
        </button>
        <div class="hidden text-sm text-white/80 lg:flex space-x-4">
          <NuxtLink to="/faq" @click="toggleMobileMenu">
            FAQ
          </NuxtLink>
          <NuxtLink to="/contacts" @click="toggleMobileMenu">
            Register a team
          </NuxtLink>
        </div>
      </div>
    </div>
    <transition name="fade">
      <div v-if="showMobileMenu" class="p-4 text-white lg:hidden divide-y">
        <NuxtLink to="/faq" class="my-2 block" @click="toggleMobileMenu">
          FAQ
        </NuxtLink>
        <NuxtLink to="/contacts" class="my-2 block" @click="toggleMobileMenu">
          Register a team
        </NuxtLink>
      </div>
    </transition>
  </div>
</template>

<style scoped>
.nav-container {
  position: sticky;
  top: 0;
  z-index: 1000;
  background-color: rgba(0, 0, 0, 0);
  backdrop-filter: blur(2px);
}

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
