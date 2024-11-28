<template>
  <main class="container">
    <SectionIntroduction />

    <template v-for="item in [1, 2, 3, 4, 5, 6, 7, 8, 9, 0]" :key="item">
      <PlaceholderSection />
    </template>
  </main>
</template>

<script setup>
import SectionIntroduction from "./components/SectionIntroduction.vue";
import PlaceholderSection from "@/components/PlaceholderSection.vue";
</script>

<style scoped></style>
