<template>
  <section class="home-section">
    <img src="/me.webp" alt="Picture of myself." class="me-picture" />

    <article>
      <h1>
        Hello World! <br />
        I'm
        <span class="name"
          >Eduardo Eiji
          <a
            href="https://en.wikipedia.org/wiki/Goto"
            target="_blank"
            rel="noopener noreferrer"
            >Goto</a
          ></span
        >
      </h1>

      <p>
        Just a chill Developer from
        <a
          href="https://en.wikipedia.org/wiki/Curitiba"
          target="_blank"
          rel="noopener noreferrer"
          >Curitiba</a
        >. <br />
        Trying to make the world a better place, one
        <span class="line-through">div</span> element at a time.
      </p>

      <div class="button-group">
        <a
          v-for="link in socialLinks"
          :key="link.label + link.to"
          :href="link.to"
          target="_blank"
          rel="noopener noreferrer"
          class="social-link"
        >
          <span>{{ link.label }}</span>
        </a>
      </div>
    </article>
  </section>
</template>

<script setup>
const socialLinks = [
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
section {
  margin-top: 8rem;
  display: grid;
  gap: 1rem;
  grid-template-columns: auto auto;
}

.name {
  color: var(--color-primary);
  font-weight: bolder;
}

.line-through {
  text-decoration: 2px line-through;
}

p {
  font-size: 1.4rem;
  max-width: 40ch;
}

.external-link {
  height: 1rem;
  display: inline-block;
}

.button-group {
  display: flex;
  gap: 1rem;
  margin-bottom: 1rem;
  align-items: center;
}

.social-link {
  padding: 0.5rem 1rem;
  border: 2px dashed var(--color-primary);
  text-decoration: none;
}

.me-picture {
  width: 18rem;
  aspect-ratio: 1;
  object-fit: cover;
  border-radius: 100%;
}
</style>
