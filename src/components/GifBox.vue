<script setup>
defineProps({
  gif: {
    type: Object,
    required: true,
  },
});
</script>

<template>
  <div class="gif-box">
    <a :href="gif.url">
      <img class="gif-image" :src="gif.images.original.url">
    </a>
  </div>
</template>
