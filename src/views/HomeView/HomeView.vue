<template>
  <main id="main" class="container">
    <SectionIntroduction />

    <SectionAboutMe />

    <SectionWorkHistory />

    <SectionEducation />
  </main>
</template>

<script setup>
import SectionIntroduction from "./components/SectionIntroduction.vue";
import SectionAboutMe from "./components/SectionAboutMe.vue";
import SectionWorkHistory from "./components/SectionWorkHistory.vue";
import SectionEducation from "./components/SectionEducation.vue";
</script>

<style>
.home-section {
  border-bottom: 2px dashed var(--color-primary);

  h2 {
    padding-top: 4rem;
    transform: translateX(-1ch);
    margin-bottom: 1rem;
  }

  h2 > a > span:first-child {
    color: var(--color-primary);
  }

  h3 {
    line-height: 1;
  }

  h3 > span {
    font-size: 1rem;
    color: var(--color-umber);
  }

  h4 {
    color: var(--color-umber);
  }

  p {
    margin-bottom: 1rem;
  }

  header {
    margin-bottom: 1rem;
  }

  section:not(:last-child) {
    margin-bottom: 2rem;
  }
}
</style>
