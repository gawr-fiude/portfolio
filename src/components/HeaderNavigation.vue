<template>
  <header class="header">
    <div class="[ header__inner ] [ container ]">
      <a id="skip-to-content" class="header__title" href="#main">
        <span>{{ `<` }}</span
        >skip-to-content <span>{{ `/>` }}</span>
      </a>

      <a href="/" class="header__title">
        <span>{{ `<` }}</span
        >goto-eduardo <span>{{ `/>` }}</span>
      </a>

      <nav class="header__nav">
        <template v-for="link in navLinks" :key="link.label + link.to">
          <a v-if="link.to.startsWith('#')" :href="link.to">
            {{ link.label }}
          </a>

          <a v-else :href="link.to" target="_blank" rel="noopener noreferrer">
            <span
              >{{ link.label }} <IconExternalLink class="external-link" />
            </span>
          </a>
        </template>
      </nav>
    </div>
  </header>
</template>

<script setup>
import IconExternalLink from "@/components/icons/IconExternalLink.vue";

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
  {
    label: "Github",
    to: "https://github.com/gawr-fiude",
  },
  {
    label: "Linkedin",
    to: "https://www.linkedin.com/in/eduardo-eiji-goto-926702217",
  },
];
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
  }

  .header__title {
    font-weight: bolder;
    font-size: 1.2rem;
    text-decoration: none;
  }

  .header__title > span {
    color: var(--color-primary);
  }

  nav {
    display: flex;
    gap: 2rem;
    align-items: center;
  }
}

.external-link {
  height: 1rem;
  display: inline-block;
}
</style>
