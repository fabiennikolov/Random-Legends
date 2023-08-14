<script setup lang="ts">
const form = reactive({
  email: '',
})

const submitted = ref(false)

const isFormFilled = computed(() => {
  return Object.values(reactiveOmit(form)).every(field => !!field)
})
async function submit() {
  if (!isFormFilled.value)
    return

  submitted.value = true
  form.reset()
}
</script>

<template>
  <form class="mxa my-10 max-w-275 rounded-3" @submit.prevent="submit">
    <div class="grid mx-auto max-w-330 overflow-hidden b-1 b-white/7 rounded-2 bg-gray/7 text-white md:grid-cols-2">
      <img src="/esport3.jpg" alt="Newsletter image" class="w-full md:h-full md:object-cover">
      <div class="px-6 py-10 space-y-8">
        <div>
          <h3 class="text-center text-6 font-bold leading-7 md:text-7">
            Subscribe and receive notifications for Upcoming tournaments
          </h3>
          <p class="mt-2 text-center text-white/80 lt-md:text-3.5">
            We wont spam you, pinky promise
          </p>
        </div>
        <div space-y-3="">
          <FormInput id="Email" v-model="form.email" type="email" placeholder="Email" mb-4 />

          <button class="w-full flex items-center justify-center gap-2 border-1 rounded-full px-2 py-3 text-4.5 font-500 text-white/80 hover:bg-white/7">
            <span uppercase lt-md:text-3.5>Subscribe</span>
          </button>
          <p v-if="submitted" class="mt5 text-green-5">
            Thank you for subscribing !
          </p>
        </div>
      </div>
    </div>
  </form>
</template>
