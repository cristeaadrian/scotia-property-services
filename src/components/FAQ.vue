<template>
  <div class="bg-white">
    <div class="mx-auto max-w-7xl py-16 px-4 sm:px-6 lg:py-20 lg:px-8">
      <div class="lg:grid lg:grid-cols-3 lg:gap-8">
        <div>
          <h2 class="text-3xl font-bold tracking-tight text-gray-900">
            Frequently asked questions
          </h2>
          <p class="mt-4 text-lg text-gray-500">
            Can’t find the answer you’re looking for? Reach out to our
            <a
              href="#"
              class="font-medium text-indigo-600 hover:text-indigo-500"
              >customer support</a
            >
            team.
          </p>
        </div>
        <div class="mt-12 lg:col-span-2 lg:mt-0">
          <dl class="space-y-12">
            <div v-for="faq in faqs" :key="faq.question">
              <dt class="text-lg font-medium leading-6 text-gray-900">
                {{ faq.question }}
              </dt>
              <dd class="mt-2 text-base text-gray-500">{{ faq.answer }}</dd>
            </div>
          </dl>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const faqs = [
  {
    id: 1,
    question: "Is Neil the best person on the planet?",
    answer: "He sure thinks so!",
  },
  {
    id: 2,
    question: "What's the best thing about Switzerland?",
    answer:
      "I don't know, but the flag is a big plus. Lorem ipsum dolor sit amet consectetur adipisicing elit. Quas cupiditate laboriosam fugiat.",
  },
  {
    id: 3,
    question: "How do you make holy water?",
    answer:
      "You boil the hell out of it. Lorem ipsum dolor sit amet consectetur adipisicing elit. Quas cupiditate laboriosam fugiat.",
  },
  {
    id: 4,
    question: "What do you call someone with no body and no nose?",
    answer:
      "Nobody knows. Lorem ipsum dolor sit amet consectetur adipisicing elit. Culpa, voluptas ipsa quia excepturi, quibusdam natus exercitationem sapiente tempore labore voluptatem.",
  },
];
</script>
