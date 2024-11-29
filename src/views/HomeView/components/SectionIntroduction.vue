<template>
  <section class="home-section">
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
  </section>
</template>

<script setup></script>

<style scoped>
section {
  margin-top: 8rem;
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
</style>
