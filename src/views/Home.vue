src/views/Home.vue
<template>
  <main class="home">

    <section class="hero">


      <div class="hero-content">

        <div class="established">
          <span></span>
          BUILT ON DREAMS, DRIVEN BY PURPOSE
        </div>

        <h1>
          JOCRE
          <em>University</em>
        </h1>

        <div class="gold-line"></div>

        <p>
          A multidisciplinary community for curious minds and purposeful futures.
          JOCRE University brings together technology, business, education, health,
          engineering, and the arts to help every learner create positive change.
        </p>

        <div class="buttons">
          <RouterLink class="primary" to="/academics">
            Explore Academics
          </RouterLink>

          <RouterLink class="secondary" to="/contact">
            Request Information
          </RouterLink>
        </div>

  
        <div class="stats">

          <div>
            <h2>6</h2>
            <p>Colleges</p>
          </div>

          <div>
            <h2>18</h2>
            <p>Undergraduate Programs</p>
          </div>

          <div>
            <h2>5</h2>
            <p>Core Values</p>
          </div>

          <div>
            <h2>1</h2>
            <p>Shared Purpose</p>
          </div>

        </div>

      </div>



      <div class="hero-image">

        <div class="image-card">

          <img
            src="../assets/jocre-crest.svg"
            alt="JOCRE University crest"
          />

          <h2>
            JOCRE<br />
            University
          </h2>

          <h4>BUILT ON DREAMS</h4>

          <div class="small-line"></div>

          <p>
            “Driven by Purpose.”
          </p>

        </div>

      </div>

    </section>

    <section class="home-section admissions-preview">
      <div>
        <p class="section-label">Admissions</p>
        <h2>Begin your university journey.</h2>
      </div>
      <div>
        <p class="section-copy">
          Find your path at a university committed to quality, accessible, and inclusive education.
          Explore scholarship support, application guidance, and the programs that fit your goals.
        </p>
        <RouterLink class="section-link" to="/admissions">View admissions information</RouterLink>
      </div>
    </section>

    <section class="home-section content-grid">
      <article>
        <p class="section-label">About Us</p>
        <h2>Learning with purpose.</h2>
        <p class="section-copy">We develop competent, responsible, and globally minded graduates who use knowledge and creativity to create positive change.</p>
        <RouterLink class="section-link" to="/about">Discover our story</RouterLink>
      </article>
      <article>
        <p class="section-label">Academics</p>
        <h2>Find your direction.</h2>
        <p class="section-copy">Choose from undergraduate programs across technology, business, education, health, engineering, and communication.</p>
        <RouterLink class="section-link" to="/academics">Explore programs</RouterLink>
      </article>
      <article>
        <p class="section-label">Campus Life</p>
        <h2>Grow beyond the classroom.</h2>
        <p class="section-copy">Find your people through student organizations, community extension, digital learning, research, and campus activities.</p>
        <RouterLink class="section-link" to="/campus-life">See campus life</RouterLink>
      </article>
    </section>

    <section class="home-section news-preview">
      <div>
        <p class="section-label">News</p>
        <h2>Learning that reaches beyond campus.</h2>
      </div>
      <RouterLink class="section-link" to="/news">Read the latest news</RouterLink>
    </section>

  </main>
</template>

<style scoped>

.home {
  min-height: calc(100vh - 90px);
}

.hero {
  min-height: 50vh;
  display: flex;
  align-items: center;
  padding: 40px 60px;
  gap: 50px;
  box-sizing: border-box;
}



.hero-content {
  width: 50%;
}

.established {
  color: #a8752d;
  font-size: 15px;
  font-weight: bold;
  letter-spacing: 2px;
  display: flex;
  align-items: center;
  gap: 15px;
}

.established span {
  width: 45px;
  height: 2px;
  background: #b59a45;
}

h1 {
  color: #780e1c;
  font-family: Georgia, serif;
  font-size: 55px;
  line-height: 1.05;
  margin: 35px 0 25px;
}

h1 em {
  color: #a8752d;
  font-weight: normal;
}

.gold-line {
  width: 60px;
  height: 3px;
  background: #c8943d;
  margin-bottom: 25px;
}

.hero-content > p {
  color: #4d4d4d;
  font-size: 17px;
  line-height: 1.8;
  max-width: 600px;
}

.hero-content strong {
  color: #780e1c;
}

/* BUTTONS */

.buttons {
  display: flex;
  gap: 25px;
  margin-top: 25px;
}

.primary,
.secondary {
  padding: 18px 30px;
  font-size: 16px;
  font-weight: bold;
  border-radius: 5px;
  cursor: pointer;
  text-decoration: none;
  display: inline-block;
}

.primary {
  background: #780e1c;
  color: white;
  border: none;
}

.secondary {
  background: white;
  color: #780e1c;
  border: 1px solid #b7925a;
}



.stats {
  margin-top: 35px;
  padding: 20px;
  display: flex;
  justify-content: space-around;
  background: white;
  border-radius: 12px;
  box-shadow: 0 5px 20px rgba(0,0,0,0.08);
}

.stats div {
  text-align: center;
  padding: 0 20px;
  border-right: 1px solid #ddd;
}

.stats div:last-child {
  border-right: none;
}

.stats h2 {
  color: #780e1c;
  margin: 0;
  font-size: 25px;
}

.stats p {
  margin: 8px 0 0;
  font-size: 12px;
  color: #555;
}



.hero-image {
  width: 50%;
  display: flex;
  justify-content: center;
}

.image-card {
  width: 85%;
  height: 500px;
  border-radius: 20px;
  background: linear-gradient(
    135deg,
    #f1c744,
    #fffdf3 45%,
    #f7f2df
  );

  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;

  box-shadow: 0 8px 25px rgba(0,0,0,0.12);
  text-align: center;
}

.image-card img {
  width: 150px;
  height: 150px;
  object-fit: contain;
}

.image-card h2 {
  color: #780e1c;
  font-family: Georgia, serif;
  font-size: 32px;
  line-height: 1.2;
}

.image-card h4 {
  color: #a8752d;
  letter-spacing: 5px;
  margin: 5px;
}

.small-line {
  width: 70px;
  height: 2px;
  background: #c8943d;
  margin: 20px;
}

.image-card p {
  font-family: Georgia, serif;
  font-style: italic;
  color: #444;
  font-size: 18px;
  line-height: 1.5;
}

.home-section {
  max-width: 1280px;
  margin: 0 auto;
  padding: 72px 60px;
}

.admissions-preview,
.news-preview {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 50px;
  align-items: end;
  border-top: 1px solid #e4e0ed;
}

.admissions-preview {
  background: #fbf8f1;
  max-width: none;
  padding-left: max(60px, calc((100% - 1280px) / 2 + 60px));
  padding-right: max(60px, calc((100% - 1280px) / 2 + 60px));
}

.content-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 28px;
}

.content-grid article {
  padding: 28px;
  border: 1px solid #e6dcc9;
  border-radius: 8px;
}

.section-label {
  color: #a8752d;
  font-size: 13px;
  font-weight: 700;
  letter-spacing: 2px;
  text-transform: uppercase;
}

.home-section h2 {
  color: #780e1c;
  font-family: Georgia, serif;
  font-size: 32px;
  margin: 12px 0 16px;
}

.section-copy {
  color: #555;
  line-height: 1.7;
}

.section-link {
  color: #780e1c;
  font-weight: 700;
  text-decoration: none;
}

.section-link:hover {
  color: #a8752d;
}


@media (max-width: 1000px) {

  .navbar {
    padding: 15px 25px;
  }

  .nav-links {
    gap: 12px;
  }

  .hero {
    flex-direction: column;
  }

  .hero-content,
  .hero-image {
    width: 100%;
  }

  .hero-image {
    margin-top: 30px;
  }

  .home-section,
  .admissions-preview {
    padding-left: 25px;
    padding-right: 25px;
  }

  .content-grid {
    grid-template-columns: 1fr;
  }

  .admissions-preview,
  .news-preview {
    grid-template-columns: 1fr;
    gap: 10px;
  }

}

</style>