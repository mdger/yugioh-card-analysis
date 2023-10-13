<script setup lang="ts">
import cardInfoRaw from "./../assets/CardInfoRaw";
import SearchEngine from "./../modules/search/SearchEngine";

const searchEngine = new SearchEngine();
searchEngine.maxResults;
const cards = cardInfoRaw.data;
defineProps<{ msg: string }>()

</script>

<template>
  <h1>{{ msg }}</h1>

  <div class="card">
    <p>
      <code>{{ cards[0] }}</code>
      <img :src="cards[0].card_images[0].image_url" />
    </p>
  </div>

  <p>
    Check out
    <a href="https://vuejs.org/guide/quick-start.html#local" target="_blank"
      >create-vue</a
    >, the official Vue + Vite starter
  </p>
  <p>
    Install
    <a href="https://github.com/vuejs/language-tools" target="_blank">Volar</a>
    in your IDE for a better DX
  </p>
  <p class="read-the-docs">Click on the Vite and Vue logos to learn more</p>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
