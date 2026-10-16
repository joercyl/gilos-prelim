<script setup>
</script>

<template>
  <nav class="navbar">
    <div class="brand">
      <img class="brand-crest" src="../assets/jocre-crest.svg" alt="" />
      <div class="school-name">
        <h2>JOCRE</h2>
        <p>University</p>
      </div>
    </div>

    <div class="nav-links">
      <router-link to="/">Home</router-link>
      <router-link to="/about">About</router-link>
      <router-link to="/academics">Academics</router-link>
      <router-link to="/admissions">Admissions</router-link>
      <router-link to="/contact">Contact</router-link>
      <router-link to="/portal-login">Portal Login</router-link>
    </div>
  </nav>
</template>

<style scoped>
.navbar {
  min-height: 70px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 10px 30px;
  background: #ffffff;
  border-bottom: 1px solid #dddddd;
}

.brand {
  display: flex;
  align-items: center;
  gap: 12px;
}

.brand-crest {
  width: 42px;
  height: 48px;
  object-fit: contain;
}

.school-name h2 {
  margin: 0;
  color: #780e1c;
  font-family: Georgia, serif;
  font-size: 21px;
  letter-spacing: 2px;
}

.school-name p {
  margin: 3px 0 0;
  font-size: 12px;
  color: #666;
}

.nav-links {
  display: flex;
  align-items: center;
  gap: 18px;
}

.nav-links a {
  text-decoration: none;
  color: #333333;
  font-weight: 500;
}

.nav-links a:hover {
  color: #8b6a3c;
}

.nav-links a.router-link-active {
  color: #780e1c;
  font-weight: 600;
}

.portal-btn {padding: 10px 18px;
background: #780e1c;
color: white !important;
border-radius: 6px;}

.portal-btn:hover {background: #5d0914;}

@media (max-width: 800px) {
  .navbar {
    align-items: flex-start;
    flex-direction: column;
    gap: 12px;
  }

  .nav-links {
    flex-wrap: wrap;
  }
}
</style>