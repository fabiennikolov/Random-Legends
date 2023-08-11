<script setup lang="ts">
interface FaqItem {
  question: string
  answer: string
  showAnswer: boolean
}

const form = reactive({
  email: '',
})

const faqItems = ref<FaqItem[]>([
  {
    question: 'How do i register my team ?',
    answer: 'You can use the contact form or connect with us in discord',
    showAnswer: false,
  },
  {
    question: 'How do i know if im eligible for rewards',
    answer: 'You can see the rules in our discord channel',
    showAnswer: false,
  },
  {
    question: 'What rewards i can earn',
    answer: 'There are variety of rewards, such as cash, RP and more !',
    showAnswer: false,
  },
])

function toggleAnswer(faq: FaqItem) {
  faq.showAnswer = !faq.showAnswer
}
</script>

<template>
  <div class="mx-auto mt-15 p-6 text-center container">
    <h1 class="mb-10 text-3xl font-semibold">
      Frequently Asked Questions
    </h1>
    <ul class="space-y-10">
      <li v-for="(faq, index) in faqItems" :key="index">
        <h2 class="inline cursor-pointer b-1 b-white rounded-3 px1.5 py2 text-16px lg:(px-3 py-3 text-lg)" @click="toggleAnswer(faq)">
          {{ faq.question }}
        </h2>
        <p v-if="faq.showAnswer" class="mt5 text-sm text-gray2 lg:text-lg">
          {{ faq.answer }}
        </p>
      </li>
    </ul>
  </div>
  <div grid mxa mt15 justify-center>
    <h1 text-7>
      Sign up for our newsletter
    </h1>
    <FormInput id="Email" v-model="form.email" type="email" placeholder="Email" />
  </div>
</template>

<style>

</style>
