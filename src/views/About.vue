<template>
  <main class="about-page">
    <section class="about-intro">
      <p class="eyebrow">About JOCRE</p>
      <h1>Built on Dreams,<br /><em>Driven by Purpose.</em></h1>
      <p>We are a multidisciplinary university preparing people to meet a changing world with knowledge, creativity, and care.</p>
    </section>

    <section class="purpose-grid" aria-label="Our vision and mission">
      <article>
        <p class="eyebrow">Our Vision</p>
        <h2>Positive change through knowledge.</h2>
        <p>To be a leading and innovative university that develops competent, responsible, and globally competitive individuals who create positive change in society through knowledge, creativity, and excellence.</p>
      </article>
      <article>
        <p class="eyebrow">Our Mission</p>
        <h2>Education with opportunity and purpose.</h2>
        <p>JOCRE University is committed to providing quality, accessible, and inclusive education that empowers students with the knowledge, skills, and values they need to succeed. We promote innovation, critical thinking, leadership, and social responsibility while preparing graduates for a changing world.</p>
      </article>
    </section>

    <section class="values-section">
      <p class="eyebrow">Our Core Values</p>
      <h2>What guides us</h2>
      <div class="values-grid">
        <article><h3>Excellence</h3><p>We strive to give our best in learning, teaching, and serving others.</p></article>
        <article><h3>Integrity</h3><p>We practice honesty, respect, and accountability in everything we do.</p></article>
        <article><h3>Innovation</h3><p>We encourage creativity, new ideas, and the responsible use of technology.</p></article>
        <article><h3>Service</h3><p>We inspire students to help their communities and make a meaningful difference.</p></article>
        <article><h3>Inclusivity</h3><p>We respect diversity and create a welcoming environment where everyone can learn.</p></article>
      </div>
    </section>

    <section class="services-section">
      <p class="eyebrow">Beyond the Classroom</p>
      <h2>What JOCRE University offers</h2>
      <ul class="services-list">
        <li><strong>Scholarship Programs</strong><span>Financial assistance for deserving students.</span></li>
        <li><strong>Research and Innovation Center</strong><span>Support for student research and creative projects.</span></li>
        <li><strong>Career Development Office</strong><span>Career guidance, internships, and job preparation.</span></li>
        <li><strong>Student Organizations</strong><span>Opportunities for leadership, teamwork, and involvement.</span></li>
        <li><strong>Community Extension Programs</strong><span>Connect learning with meaningful community service.</span></li>
        <li><strong>Digital Learning Facilities</strong><span>Computer laboratories, online resources, and modern classrooms.</span></li>
      </ul>
    </section>
  </main>
</template>

<style scoped>
.about-page {
  color: #352b27;
  background: #fbf8f1;
}

.about-intro,
.purpose-grid,
.values-section,
.services-section {
  max-width: 1160px;
  margin: 0 auto;
  padding: 76px 32px;
}

.about-intro {
  padding-top: 90px;
  padding-bottom: 64px;
}

.eyebrow {
  margin: 0 0 12px;
  color: #a8752d;
  font-size: 13px;
  font-weight: 700;
  text-transform: uppercase;
}

h1,
h2,
h3 {
  color: #780e1c;
  font-family: Georgia, serif;
}

h1 {
  margin: 0;
  font-size: 48px;
  line-height: 1.12;
}

h1 em {
  color: #a8752d;
  font-weight: 400;
}

.about-intro > p:last-child,
.purpose-grid p:not(.eyebrow),
.values-grid p,
.services-list span {
  color: #65594e;
  line-height: 1.75;
}

.about-intro > p:last-child {
  max-width: 650px;
  font-size: 18px;
}

.purpose-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 64px;
  border-top: 1px solid #e6dcc9;
  border-bottom: 1px solid #e6dcc9;
}

h2 {
  margin: 0 0 14px;
  font-size: 29px;
}

.values-section > h2,
.services-section > h2 {
  margin-bottom: 30px;
}

.values-grid {
  display: grid;
  grid-template-columns: repeat(5, minmax(0, 1fr));
  gap: 18px;
}

.values-grid article {
  padding-top: 16px;
  border-top: 3px solid #c8943d;
}

h3 {
  margin: 0 0 8px;
  font-size: 21px;
}

.values-grid p {
  margin: 0;
  font-size: 14px;
}

.services-section {
  max-width: none;
  padding-right: max(32px, calc((100% - 1096px) / 2));
  padding-left: max(32px, calc((100% - 1096px) / 2));
  background: #f2eadb;
}

.services-list {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 0 48px;
  margin: 0;
  padding: 0;
  list-style: none;
}

.services-list li {
  display: flex;
  flex-direction: column;
  gap: 4px;
  padding: 18px 0;
  border-top: 1px solid #d9c8aa;
}

.services-list strong {
  color: #780e1c;
}

@media (max-width: 800px) {
  .values-grid {
    grid-template-columns: repeat(2, minmax(0, 1fr));
  }

  .purpose-grid {
    gap: 36px;
  }
}

@media (max-width: 560px) {
  .about-intro,
  .purpose-grid,
  .values-section,
  .services-section {
    padding: 48px 22px;
  }

  h1 {
    font-size: 38px;
  }

  .purpose-grid,
  .services-list {
    grid-template-columns: 1fr;
  }

  .values-grid {
    grid-template-columns: 1fr 1fr;
  }
}
</style>

