<script setup>
import { ref } from "vue";
const show = ref(true);
const attachRed = ref(false);
</script>
<template>
  <main class="main">
    <!--<br />-->
    <p>Click on box to change its color <br />↓↓↓</p>
    <div
      class="demo"
      @click="attachRed = !attachRed"
      v-bind:class="{ red: attachRed }"
    ></div>
    <br />
    <p><button @click="show = !show">Click to interact</button></p>
    <p v-if="show">Can you see me?</p>
    <p v-else>Flying away!</p>
    <img
      v-if="show"
      src="https://t3.ftcdn.net/jpg/00/36/83/88/360_F_36838861_UHfFCcgipUy5Orup7vniss11Ly3OLsgf.jpg"
      class="img-fluid"
      alt="bird landing"
    />
    <img
      v-else
      src="https://us.123rf.com/450wm/hermandesign2015/hermandesign20151512/hermandesign2015151200304/49057308-illustration-of-happy-flying-bird.jpg"
      class="img-fluid"
      alt="bird flying"
    /><br /><br />
  </main>
</template>
<style scoped>
main {
  text-align: center;
}
.demo {
  height: 100px;
  width: 100px;
  background-color: green;
  margin: auto;
}
.red {
  background-color: red;
  margin: auto;
}
</style>
