<template>
  <layout>
    <section class="section faqs">
      <div class="container">
        <div class="columns">
          <div class="column">
            <div class="faqs__heading">
              <h1 class="title">Frequently Asked Questions</h1>
              <p class="subtitle">
                Here's some questions that people often ask about TraceToZero.
              </p>
            </div>
            <div class="faqs__container">
              <FaqAccordion
                :items="myItems"
                borderColor="#fff"
              />
            </div>
          </div>
        </div>
      </div>
    </section>
  </layout>
</template>

<script>
import FaqAccordion from '~/components/faq/FAQAccordion.vue'
export default {
  components: {
    FaqAccordion
  },
  data() {
    return {
      myItems: [
        {
          title: 'How many time zones are there in all?',
          value:
            'Given a 24-hour day and 360 degrees of longitude around the Earth'
        },
        {
          title: 'How long is a day and year on Venus?',
          value:
            'Venus takes 224.7 Earth days to complete one orbit around the Sun.'
        },
        {
          title: 'What animal smells like popcorn?',
          value: 'Binturongs smell like popcorn.'
        }
      ]
    }
  }
}
</script>

<style scoped lang="scss">
.section {
  padding-top: 9rem;
  padding-bottom: 6rem;
}

.faqs {
  &__heading {
    text-align: center;
    padding-bottom: 4rem;
  }
  h1 {
    text-align: center;
  }

  .accordion {
    &__item {
      border: 1px solid #000;
    }
  }
}
</style>