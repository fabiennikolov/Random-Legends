<template>
  <div class="layout">
    <Nav />
    <main class="content min-h-screen pxa pya">
      <slot />
    </main>
    <Footer />
  </div>
</template>

<style scoped>
.layout {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

.content {
  flex: 1; /* main contenta se raztqga i vzima ostanaloto prostranstvo */
}
</style>
