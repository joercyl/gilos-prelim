<template>
  <main class="lesson-page">
    <h1>Student Profile</h1>
    <p>Name: {{ name }}</p>
    <p>Age: {{ age }}</p>
    <p>Student ID: {{ studentId }}</p>
    <p>Course: {{ course }}</p>
    <p>Year Level: {{ yearLevel }}</p>
  </main>
</template>

<script>
export default {
  data() {
    return {
      name: 'Joercyl Faith',
      age: 20,
      studentId: '24-0120-15',
      course: 'BSIT',
      yearLevel: '3rd Year'
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
</style>
