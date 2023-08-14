<script setup lang="ts">
const form = reactive({
  email: '',
})
</script>

<template>
  <div grid mxa mt15 justify-center>
    <h1 text-7>
      Sign up for our newsletter
    </h1>
    <FormInput id="Email" v-model="form.email" type="email" placeholder="Email" />
    <button
      class="relative mt10 w-full b-1 b-gray rounded-full bg-black/2 px-5 py-4 text-center font-500 text-white transition-colors-250 after:absolute after:z-0 hover:bg-gray/9 after:transition-all-250 hover:after:opacity-65" type="submit"
    >
      Send
    </button>
  </div>
</template>
