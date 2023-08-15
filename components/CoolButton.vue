<template>
  <button
    type="submit" class="group relative isolate overflow-hidden btn"
  >
    <div
      class="absolute -inset-4 -z-1"
      bg-white text="#222222" rounded="50%"
      transition-all-500 translate-y="80%" group-hover="translate-y-0"
      flex items-center justify-center
    >
      <slot />
    </div>
    <span class="invisible">
      <slot />
    </span>
    <span
      absolute inset-0
      transition-all-500 group-hover="-translate-y-50% opacity-0"
      flex items-center justify-center
    >
      <slot />
    </span>
  </button>
</template>
