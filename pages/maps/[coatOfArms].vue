<script setup>
import { useRoute } from "vue-router";
const route = useRoute();
const coatOfArms = route.params.coatOfArms;
</script>
<template>
  <img :src="coatOfArms" alt="coatOfArms"/>
</template>