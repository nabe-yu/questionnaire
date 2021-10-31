<template>
  <section>
    <div class="card p-4">
      <b-field label="質問1：あなたはほげほげですか。" />
      <Radio />
      <Checkbox />
      <NumberInput />
      <TextInput />
      <Select />
    </div>
  </section>
</template>

<script>
import Radio from '~/components/choices/radio.vue'
import Checkbox from '~/components/choices/checkbox.vue'
import NumberInput from '~/components/choices/number_input.vue'
import TextInput from '~/components/choices/text_input.vue'
import Select from '~/components/choices/select.vue'
export default {
  components: { Radio, Checkbox, NumberInput, TextInput, Select }
}
</script>
