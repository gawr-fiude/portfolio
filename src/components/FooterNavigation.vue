<template>
  <footer class="container">
    <div class="quote">
      <blockquote>
        <p>
          Yesterday is history,<br />
          tomorrow is a mystery,<br />
          but today is a gift, that is why it is called the present.
        </p>
      </blockquote>

      <p>- Oogway</p>
    </div>

    <div class="circle-group">
      <div class="circle text"></div>
      <div class="circle primary"></div>
      <div class="circle umber"></div>
      <div class="circle peach"></div>
    </div>
  </footer>
</template>

<script setup></script>

<style scoped>
footer {
  margin-top: 4rem;
  margin-bottom: 2rem;
}

.quote {
  color: var(--color-umber);
  border: 2px dashed var(--color-primary);
  padding: 2rem;
}

blockquote {
  margin-bottom: 1rem;
}

.circle-group {
  display: flex;
  gap: 0.2rem;
  margin-top: 1rem;
}

.circle {
  height: 1.5rem;
  aspect-ratio: 1;
}

.text {
  background: var(--color-text);
}

.primary {
  background: var(--color-primary);
}

.umber {
  background: var(--color-umber);
}

.peach {
  background: var(--color-peach);
}
</style>
