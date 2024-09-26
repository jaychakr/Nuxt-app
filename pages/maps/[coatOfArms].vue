<script setup>
import { useRoute } from "vue-router";
const route = useRoute();
const coatOfArms = route.params.coatOfArms;
</script>
<template>
  <div class="container">
    <img :src="coatOfArms" alt="coatOfArms" width="275px"/>
  </div>
</template>
<style scoped>
.container {
  display: flex;
  justify-content: center;
}
</style>
