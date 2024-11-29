<template>
  <main id="main" class="container">
    <SectionIntroduction />

    <h2 id="about-me">About Me</h2>
    <PlaceholderSection v-for="item in [1, 2, 3, 4]" :key="item" />

    <h2 id="curriculum">Resumé</h2>
    <PlaceholderSection v-for="item in [1, 2, 3, 4]" :key="item" />

    <h2 id="education">Education</h2>
    <PlaceholderSection v-for="item in [1, 2, 3, 4]" :key="item" />
  </main>
</template>

<script setup>
import SectionIntroduction from "./components/SectionIntroduction.vue";
import PlaceholderSection from "@/components/PlaceholderSection.vue";
</script>

<style scoped>
h2 {
  padding-top: 4rem;
}
</style>
