<template>
  <main class="academics-page">
    <header class="academics-intro">
      <p class="eyebrow">Academics</p>
      <h1>Find your field.<br /><em>Shape what comes next.</em></h1>
      <p>Explore practical, future-focused programs across six colleges, designed to build knowledge, creativity, and confidence.</p>
    </header>

    <section class="college-grid" aria-label="Colleges and undergraduate programs">
      <article class="college">
        <p class="college-number">01</p>
        <h2>Information Technology and Computing</h2>
        <ul><li>BS Information Technology</li><li>BS Computer Science</li><li>BS Information Systems</li></ul>
      </article>
      <article class="college">
        <p class="college-number">02</p>
        <h2>Business and Management</h2>
        <ul><li>BS Business Administration</li><li>BS Accountancy</li><li>BS Entrepreneurship</li></ul>
      </article>
      <article class="college">
        <p class="college-number">03</p>
        <h2>Education</h2>
        <ul><li>Bachelor of Elementary Education</li><li>Bachelor of Secondary Education</li><li>Bachelor of Early Childhood Education</li></ul>
      </article>
      <article class="college">
        <p class="college-number">04</p>
        <h2>Health Sciences</h2>
        <ul><li>BS Nursing</li><li>BS Medical Technology</li><li>BS Psychology</li></ul>
      </article>
      <article class="college">
        <p class="college-number">05</p>
        <h2>Engineering and Technology</h2>
        <ul><li>BS Computer Engineering</li><li>BS Electronics Engineering</li><li>BS Civil Engineering</li></ul>
      </article>
      <article class="college">
        <p class="college-number">06</p>
        <h2>Arts and Communication</h2>
        <ul><li>BA Communication</li><li>BA Multimedia Arts</li><li>BA English Language Studies</li></ul>
      </article>
    </section>

    <section class="learning-note">
      <p class="eyebrow">Your next step</p>
      <h2>Learn with purpose. Graduate ready to contribute.</h2>
      <RouterLink to="/admissions">Explore admissions <span aria-hidden="true">→</span></RouterLink>
    </section>
  </main>
</template>

<style scoped>
.academics-page {
  background: #fbf8f1;
  color: #352b27;
}

.academics-intro,
.college-grid,
.learning-note {
  max-width: 1160px;
  margin: 0 auto;
  padding: 68px 32px;
}

.academics-intro {
  padding-top: 90px;
  padding-bottom: 56px;
}

.eyebrow,
.college-number {
  margin: 0 0 12px;
  color: #a8752d;
  font-size: 13px;
  font-weight: 700;
  text-transform: uppercase;
}

h1,
h2 {
  color: #780e1c;
  font-family: Georgia, serif;
}

h1 {
  margin: 0;
  font-size: 46px;
  line-height: 1.14;
}

h1 em {
  color: #a8752d;
  font-weight: 400;
}

.academics-intro > p:last-child {
  max-width: 650px;
  color: #65594e;
  font-size: 17px;
  line-height: 1.7;
}

.college-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 0 34px;
  border-top: 1px solid #e6dcc9;
}

.college {
  min-height: 210px;
  padding: 24px 0 30px;
  border-bottom: 1px solid #e6dcc9;
}

.college-number {
  margin-bottom: 10px;
}

.college h2 {
  margin: 0 0 14px;
  font-size: 23px;
  line-height: 1.25;
}

.college ul {
  margin: 0;
  padding-left: 18px;
  color: #65594e;
  line-height: 1.8;
}

.learning-note {
  max-width: none;
  padding-right: max(32px, calc((100% - 1096px) / 2));
  padding-left: max(32px, calc((100% - 1096px) / 2));
  background: #f2eadb;
}

.learning-note h2 {
  max-width: 650px;
  margin: 0 0 18px;
  font-size: 30px;
}

.learning-note a {
  color: #780e1c;
  font-weight: 700;
  text-decoration-color: #c8943d;
  text-underline-offset: 5px;
}

@media (max-width: 850px) {
  .college-grid {
    grid-template-columns: repeat(2, minmax(0, 1fr));
  }
}

@media (max-width: 560px) {
  .academics-intro,
  .college-grid,
  .learning-note {
    padding: 48px 22px;
  }

  h1 {
    font-size: 37px;
  }

  .college-grid {
    grid-template-columns: 1fr;
  }
}
</style>

