<template>
  <main class="lesson-page">
    <h1>Live Profile Form</h1>
    <form class="profile-form" @submit.prevent>
      <label>
        Name
        <input v-model="name" type="text" autocomplete="name">
      </label>
      <label>
        Age
        <input v-model="age" type="number" min="0">
      </label>
      <label>
        Course
        <input v-model="course" type="text">
      </label>
    </form>

    <section class="profile-output" aria-live="polite">
      <h2>Hello {{ name }}</h2>
      <p>Name: {{ name }}</p>
      <p>Age: {{ age }}</p>
      <p>Course: {{ course }}</p>
    </section>
  </main>
</template>

<script>
export default {
  data() {
    return {
      name: '',
      age: '',
      course: ''
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

h1,
h2 {
  color: #780e1c;
  font-family: Georgia, serif;
}

.profile-form {
  display: grid;
  gap: 16px;
  max-width: 420px;
}

label {
  display: grid;
  gap: 6px;
  font-weight: 600;
}

input {
  min-height: 42px;
  padding: 8px 10px;
  border: 1px solid #b9b1a8;
  border-radius: 4px;
  font: inherit;
}

.profile-output {
  margin-top: 28px;
}

.profile-output h2 {
  margin-bottom: 16px;
}
</style>
