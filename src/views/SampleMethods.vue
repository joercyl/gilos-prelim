<template>
  <main class="lesson-page">
    <h1>Counter</h1>
    <h2 aria-live="polite">{{ count }}</h2>
    <div class="buttons">
      <button type="button" @click="decrease">-</button>
      <button type="button" @click="increase">+</button>
    </div>
  </main>
</template>

<script>
export default {
  data() {
    return {
      count: 0
    }
  },
  methods: {
    increase() {
      this.count++
    },
    decrease() {
      this.count--
    }
  }
}
</script>

<style scoped>
.lesson-page {
  max-width: 720px;
  margin: 48px auto;
  padding: 32px;
  color: #352b27;
}

h1 {
  color: #780e1c;
  font-family: Georgia, serif;
}

.buttons {
  display: flex;
  gap: 12px;
}

button {
  min-width: 44px;
  min-height: 44px;
  border: 0;
  border-radius: 6px;
  background: #780e1c;
  color: #fff;
  font-size: 20px;
  cursor: pointer;
}
</style>
