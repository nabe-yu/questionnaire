<template>
  <section>
    <div class="content">
      <h4>アンケート</h4>
    </div>
    <div v-for="questionnaire in questionnaires" :key="questionnaire.id" class="p-3">
      <b-button
        type="is-primary is-large"
        outlined
        expanded
        @click="a"
      >
        <span>{{ questionnaire.title }}</span>
      </b-button>
    </div>
  </section>
</template>

<script>
export default {
  async asyncData ({ $axios }) {
    return {
      questionnaires: await $axios.$get('http://localhost:3301/questionnaires')
    }
  }
}
</script>
