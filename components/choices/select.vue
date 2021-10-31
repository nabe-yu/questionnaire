<template>
  <section>
    <b-field>
      <b-select placeholder="Select a name" expanded>
        <option
          v-for="option in data"
          :key="option.id"
          :value="option.id"
        >
          {{ option.user.first_name }}
        </option>
      </b-select>
    </b-field>
  </section>
</template>
