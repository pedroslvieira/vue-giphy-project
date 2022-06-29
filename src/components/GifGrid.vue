<script setup>
import GifBox from "@/components/GifBox.vue";

defineProps({
  gifs: {
    type: Array,
    required: true,
  },
});
</script>

<template>
  <div class="columns is-multiline" v-if="gifs">
    <div class="column is-one-third" v-for="gif in gifs">
      <GifBox :gif="gif" />
    </div>
  </div>
</template>
