<script setup>
const query = "";

const goToAbout = () => {

}
</script>

<template>
  <div class="search-bar">
    <input
      type="text"
      @submit.prevent="goToAbout"
      v-model="query"
      class="input"
      name="query"
    />
    <button>Submit</button>
  </div>
</template>
