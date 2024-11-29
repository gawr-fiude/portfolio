<template>
  <main id="main" class="container">
    <SectionIntroduction />

    <SectionAboutMe />

    <h2 id="curriculum">Curriculum</h2>
    <PlaceholderSection v-for="item in [1, 2, 3, 4]" :key="item" />

    <h2 id="education">Education</h2>
    <PlaceholderSection v-for="item in [1, 2, 3, 4]" :key="item" />
  </main>
</template>

<script setup>
import SectionIntroduction from "./components/SectionIntroduction.vue";
import SectionAboutMe from "./components/SectionAboutMe.vue";

import PlaceholderSection from "@/components/PlaceholderSection.vue";
</script>

<style scoped>
h2 {
  padding-top: 4rem;
}
</style>

<style>
.home-section {
  h2 {
    padding-top: 4rem;
  }

  p {
    margin-bottom: 1rem;
  }
}
</style>
