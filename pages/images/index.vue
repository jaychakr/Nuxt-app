<script setup>
import { ref } from "vue";
import ImageComponent from "../../components/ImageComponent.vue";
const images = ref([
  {
    src: "https://images.pexels.com/photos/346529/pexels-photo-346529.jpeg?auto=compress&cs=tinysrgb&w=600",
    alt: "mountains",
    title: "Lake and Mountains",
  },
  {
    src: "https://images.pexels.com/photos/147411/italy-mountains-dawn-daybreak-147411.jpeg?auto=compress&cs=tinysrgb&w=600",
    alt: "lake",
    title: "House on Lake",
  },
  {
    src: "https://images.pexels.com/photos/247599/pexels-photo-247599.jpeg?auto=compress&cs=tinysrgb&w=600",
    alt: "greenery",
    title: "Sunlight on Mountains",
  },
  {
    src: "https://images.pexels.com/photos/709552/pexels-photo-709552.jpeg?auto=compress&cs=tinysrgb&w=600",
    alt: "river",
    title: "River in Forest",
  },
]);
</script>
<template>
  <main class="main">
    <br />
    <div v-for="image in images" :key="image.src">
      <ImageComponent
        :src="image.src"
        :alt="image.alt"
        :title="image.title"
      /><br /><br />
    </div>
  </main>
</template>
<style scoped>
.main {
  text-align: center;
}
</style>
