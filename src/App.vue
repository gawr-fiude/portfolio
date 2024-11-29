<template>
  <HeaderNavigation />

  <RouterView />

  <FooterNavigation />
</template>

<script setup>
import { RouterView } from "vue-router";
import HeaderNavigation from "./components/HeaderNavigation.vue";
import FooterNavigation from "./components/FooterNavigation.vue";
</script>

<style scoped></style>
