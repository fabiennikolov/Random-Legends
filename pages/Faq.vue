<script setup lang="ts">
interface FaqItem {
  question: string
  answer: string
  showAnswer: boolean
}

const faqItems: Ref<FaqItem[]> = ref([
  {
    question: 'How do I register my team ?',
    answer: 'You can easily register your team by filling out the registration form or contacting us through our official Discord channel.',
    showAnswer: false,
  },
  {
    question: 'Am I eligible for rewards ?',
    answer: 'To check your eligibility for rewards, please refer to the rules and guidelines provided in our Discord channel.',
    showAnswer: false,
  },
  {
    question: 'What kind of rewards can I earn ?',
    answer: 'We offer a variety of exciting rewards, including cash prizes, in-game currency, and much more!',
    showAnswer: false,
  },

])

function toggleAnswer(faq: FaqItem) {
  faq.showAnswer = !faq.showAnswer
}
</script>

<template>
  <div class="mx-auto mt-15 p-6 max-w-6xl">
    <h1 class="mb-10 text-3xl font-semibold">
      Frequently Asked Questions
    </h1>
    <ul class="space-y-6">
      <li v-for="(faq, index) in faqItems" :key="index">
        <h2
          class=" cursor-pointer bg-white/9 rounded-3 px-4 py-2 text-lg hover:bg-white/12 duration-200"
          @click="toggleAnswer(faq)"
        >
          {{ faq.question }}
          <UnoIcon
            v-if="faq.showAnswer"
            icon="i-ic-round-minus"
            class="float-right mt1"
          />
          <UnoIcon
            v-else
            icon="i-ic-round-add"
            class="float-right mt1"
          />
        </h2>
        <p v-if="faq.showAnswer" class="mt-3 ml2 text-gray-300">
          {{ faq.answer }}
        </p>
      </li>
    </ul>
  </div>
  <Newsletter />
</template>
