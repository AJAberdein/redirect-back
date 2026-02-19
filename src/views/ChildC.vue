<template>
  <div class="about">
    <h1>Page C - Nav Guard</h1>
  </div>
</template>

<script setup lang="ts">
import { onBeforeRouteLeave } from "vue-router";

onBeforeRouteLeave((to, from, next) => {
  const confirmLeave = window.confirm("Are you sure you want to go back?");

  if (confirmLeave) next();
  else next(false);
});
</script>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
