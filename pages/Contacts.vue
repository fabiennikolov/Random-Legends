<script setup lang="ts">
const form = reactive({
  name: '',
  email: '',
  number: '',
  comment: '',
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
  <h1 mt-15 text-center text-xl font-extrabold uppercase>
    Contact us to register your team
  </h1>
  <form @submit.prevent="submit">
    <div px-2>
      <div class="mxa my-2rem max-w-200 b-transparent border-[#B2BDD4] rounded-2 p-8 text-white shadow-xl drop-shadow-md">
        <FormInput id="Name" v-model="form.name" placeholder="Team Name" />
        <FormInput id="Email" v-model="form.email" type="email" placeholder="Email" />
        <FormInput id="Number" v-model="form.number" placeholder="Number" />
        <FormTextarea id="comment" v-model="form.comment" placeholder="Comment..." />
        <button
          class="relative mt10 w-full b-1 b-gray rounded-full bg-black/2 px-5 py-4 text-center font-500 text-white transition-colors-250 after:absolute after:z-0 hover:bg-gray/9 after:transition-all-250 hover:after:opacity-65" type="submit"
        >
          Send
        </button>
        <p v-if="submitted" class="mt5 text-green-5">
          Team sucessfully registered !
        </p>
      </div>
    </div>
  </form>
</template>
