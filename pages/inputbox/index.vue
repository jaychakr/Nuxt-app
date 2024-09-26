<script setup>
import { ref } from "vue";
const text = ref("Hello!");
function changeText(event) {
  text.value = event.target.value;
}
</script>
<template>
  <main>
    <br />
    <img
      alt="Vue logo"
      class="logo"
      src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/95/Vue.js_Logo_2.svg/640px-Vue.js_Logo_2.svg.png"
      width="125"
      height="125"
    />
    <h1>{{ text }}</h1>
    <p>Type into input box to see content change as you type:</p>
    <input v-model="text" @input="changeText" />
  </main>
</template>
<style scoped>
main {
  line-height: 1.5;
  text-align: center;
}
</style>
