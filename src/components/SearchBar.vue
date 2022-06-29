<script setup>
import { RouterLink, RouterView } from "vue-router";
</script>

<template>
  <form action="/about">
    <div class="search-bar">
      <input type="text" class="input" />
      <!-- <input type="submit" /> -->
      <button>
        <Router-Link to="/about"> Submit </Router-Link>
      </button>
    </div>
  </form>
</template>
