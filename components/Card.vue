<script setup>
import { defineProps } from "vue";
const animate = ref(false);
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
<template>
  <div class="card">
    <h3>{{ props.name }}</h3>
    <p>{{ props.subregion }}</p>
    <p>Capital: {{ props.capital }}</p>
    <p>
      <NuxtLink :to="`/maps/${encodedUrl}`"
        >Click Here for Coat of Arms</NuxtLink
      >
    </p>
    <img
      v-if="animate"
      @click="animate = !animate"
      :src="props.flag"
      alt="flag"
      style="border: 1px solid black"
      class="animated-img"
      width="275px"
    />
    <img
      v-else
      @click="animate = !animate"
      :src="props.flag"
      alt="flag"
      style="border: 1px solid black"
      width="275px"
    />
    <p><b>↑↑ Click on flag to see animation ↑↑</b></p>
  </div>
</template>
<style scoped>
.animated-img {
  animation: move 1.5s linear infinite;
}
@keyframes move {
  0% {
    transform: translateX(0);
  }
  25% {
    transform: translateX(-100px);
  }
  75% {
    transform: translateX(100px);
  }
  100% {
    transform: translateX(0);
  }
}
.card {
  align-items: center;
}
</style>
