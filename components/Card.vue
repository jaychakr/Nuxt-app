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
    default: "https://flagcdn.com/w320/us.png",
  },
  capital: {
    type: String,
    required: true,
    default: "Capital",
  },
  coatOfArms: {
    type: String,
    required: true,
    default: "https://mainfacts.com/media/images/coats_of_arms/us.png",
  },
});
const url = props.coatOfArms;
const encodedUrl = encodeURIComponent(url);
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
    <p>
      <NuxtLink :to="`/maps/${encodedUrl}`"
        >Click Here for Coat of Arms</NuxtLink
      >
    </p>
    <img
      v-if="border"
      :src="props.flag"
      alt="flag"
      style="border: 3px solid black"
      class="animated-img"
      width="275px"
    />
    <img v-else :src="props.flag" alt="flag" width="275px" />
    <p><b>↑↑ Click on flag to see animation ↑↑</b></p>
  </div>
</template>
<style scoped>
.animated-img {
  animation: move 1s ease infinite alternate;
  transform: translateX(0);
}

@keyframes move {
  to {
    transform: translateX(100px);
  }
}
.card {
  align-items: center;
}
</style>
