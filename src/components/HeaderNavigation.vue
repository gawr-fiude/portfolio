<template>
  <header class="header">
    <div class="[ header__inner ] [ container ]">
      <a id="skip-to-content" class="header__title" href="#main">
        <span>{{ `<` }}</span
        >skip-to-content <span>{{ `/>` }}</span>
      </a>

      <div class="header__title">
        <span>{{ `<` }}</span
        >goto-eduardo <span>{{ `/>` }}</span>
      </div>

      <nav v-if="isLargeScreen" class="header__nav">
        <a v-for="link in navLinks" :key="link.label + link.to" :href="link.to">
          {{ link.label }}
        </a>
      </nav>

      <button
        v-else
        class="mobile-nav__button"
        @click="openNavigation = !openNavigation"
      >
        <IconMenu v-if="!openNavigation" />
        <IconX v-else />
      </button>
    </div>

    <Transition>
      <nav v-if="openNavigation" class="header__nav--mobile">
        <a
          @click="openNavigation = false"
          v-for="link in navLinks"
          :key="link.label + link.to"
          :href="link.to"
        >
          {{ link.label }}
        </a>
      </nav>
    </Transition>
  </header>
</template>

<script setup>
import { ref } from "vue";
import { useMediaQuery } from "@vueuse/core";

import IconMenu from "@/components/icons/IconMenu.vue";
import IconX from "@/components/icons/IconX.vue";

const navLinks = [
  {
    label: "About Me",
    to: "#about-me",
  },
  {
    label: "Work History",
    to: "#work-history",
  },
  {
    label: "Education",
    to: "#education",
  },
];

const isLargeScreen = useMediaQuery("(min-width: 50rem)");
const openNavigation = ref(false);
</script>

<style scoped>
.header {
  position: sticky;
  top: 0;
  background-color: var(--color-base);
  z-index: 1;

  #skip-to-content {
    position: absolute;
    transform: translateY(-300%);
  }

  #skip-to-content:focus {
    transform: translateY(0);
  }

  .header__inner {
    display: flex;
    justify-content: space-between;
    padding: 1rem 0;
    align-items: center;
  }

  .header__title {
    font-weight: bolder;
    font-size: 1.2rem;
    text-decoration: none;
  }

  .header__title > span {
    color: var(--color-primary);
  }

  .header__nav > a:not(:last-child) {
    margin-right: 2rem;
  }

  /* Mobile Navigation */
  .mobile-nav__button {
    height: 1.5rem;
    aspect-ratio: 1;
  }

  .header__nav--mobile {
    position: absolute;
    background: var(--color-text);
    color: var(--color-base);
    width: 100dvw;
    min-height: 100dvh;

    display: flex;
    flex-direction: column;
  }

  .header__nav--mobile > a {
    padding: 1rem;
  }
}

/* Animation for mobile navigation */
.v-enter-active,
.v-leave-active {
  transition: all 0.5s ease;
}

.v-enter-from,
.v-leave-to {
  transform: translateX(100%);
}
</style>
