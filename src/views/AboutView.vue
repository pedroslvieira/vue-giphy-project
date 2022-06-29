<script setup>
import GifGrid from "@/components/GifGrid.vue";
import axios from "axios";
import { ref } from "vue";

const apiUrl = "http://api.giphy.com/v1/gifs";
const apiKey = "e86wNzbZoCqnIaVDBm0PHbwqv3JCQ5lC";
const url = `${apiUrl}/trending?api_key=${apiKey}&limit=10`;
const gifsApi = ref([]);

const loadGifs = async () => {
  const response = await axios.get(url);
  gifsApi.value = response.data.data;
};

loadGifs();
</script>

<template>
  <div class="gif-box">
    <GifGrid v-if="gifsApi" :gifs="gifsApi" />
  </div>
</template>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
