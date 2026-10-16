<script setup>
defineProps({
  title: {
    type: String,
    required: true
  },
  text: {
    type: String,
    default: 'Built on Dreams, Driven by Purpose.'
  }
})
</script>

<template>
  <main class="page-content">
    <section class="page-header">
      <p class="label">JOCRE University</p>
      <h1>{{ title }}</h1>
      <p>{{ text }}</p>
    </section>
  </main>
</template>

<style scoped>
.page-content {
  min-height: 420px;
  padding: 64px 24px;
  background: #fbf8f1;
}

.page-header {
  max-width: 900px;
  margin: 0 auto;
  padding: 36px 0;
  border-bottom: 1px solid #e6dcc9;
}

.label {
  margin: 0 0 10px;
  color: #a8752d;
  font-size: 13px;
  font-weight: 700;
  text-transform: uppercase;
}

h1 {
  margin: 0 0 16px;
  color: #780e1c;
  font-size: 32px;
  font-weight: 600;
}

.page-header p:last-child {
  max-width: 650px;
  margin: 0;
  color: #555555;
  line-height: 1.7;
}

@media (max-width: 640px) {
  .page-content {
    padding: 32px 20px;
  }

  h1 {
    font-size: 26px;
  }
}
</style>
