
<template>
  <section>
    <div class="content">
      <h2>{{ questionnaire.title }}</h2>
      <b-notification>{{ questionnaire.start_description }}</b-notification>
      <div class="hero is-info is-small">
        <div class="hero-body">
          <div class="container">
            <p class="is-small">
              {{ questionnaire.pages[0].description }}
            </p>
          </div>
        </div>
      </div>
    </div>
    <question />
    <div
      v-for="question in questionnaire.pages[0].questions"
      :key="question.id"
      class="content is-small"
    >
      <div class="box p-4">
        <h3>
          {{ question.body }}
        </h3>
        <b-field label="question.body">
          <div v-for="choice in question.choices" :key="choice.id" class="p-2">
            <b-radio v-model="radio">
              {{ choice.body }}
            </b-radio>
          </div>
        </b-field>
      </div>
    </div>
  </section>
</template>

<script>
import question from '~/components/question.vue'
export default {
  components: { question },
  async asyncData ({ $axios }) {
    return {
      questionnaire: await $axios.$get(
        'http://localhost:3301/questionnaires/1'
      )
    }
  }
}
</script>
