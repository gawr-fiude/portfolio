<template>
  <HeaderNavigation />

  <RouterView />
</template>

<script setup>
import { RouterView } from "vue-router";
import HeaderNavigation from "./components/HeaderNavigation.vue";
</script>

<style scoped></style>
