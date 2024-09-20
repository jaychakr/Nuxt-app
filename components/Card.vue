<script setup>
import { defineProps } from "vue";
import borderToggle from "./borderToggle";
const props = defineProps({
  name: {
    type: String,
    required: true,
    default: "Country",
  },
  subregion: {
    type: String,
    required: true,
    default: "Region",
  },
  flag: {
    type: String,
    required: true,
    default: "'https://flagcdn.com/w320/us.png'",
  },
  capital: {
    type: String,
    required: true,
    default: "Capital",
  },
});
</script>
<script>
export default {
  mixins: [borderToggle],
};
</script>
<template>
  <div class="card" @click="toggle">
    <h3>{{ props.name }}</h3>
    <p>{{ props.subregion }}</p>
    <p>Capital: {{ props.capital }}</p>
    <img
      v-if="border"
      :src="props.flag"
      alt="flag"
      style="border: 3px solid black"
    />
    <img v-else :src="props.flag" alt="flag" />
  </div>
</template>
<style scoped></style>
