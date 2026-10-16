<script setup>
defineProps({
  links: {
    type: Array,
    default: () => []
  },
  contact: {
    type: Object,
    default: () => ({})
  }
})
</script>

<template>
  <footer class="site-footer">
    <div class="footer-grid">
      <div>
        <p class="footer-eyebrow">JOCRE University</p>
        <p class="footer-copy">Built on Dreams, Driven by Purpose.</p>
      </div>

      <div>
        <h2>Important Links</h2>
        <nav class="footer-links" aria-label="Footer navigation">
          <RouterLink v-for="link in links" :key="link.to" :to="link.to">
            {{ link.label }}
          </RouterLink>
        </nav>
      </div>

      <div>
        <h2>Contact</h2>
        <p>{{ contact.address }}</p>
        <p>{{ contact.email }}</p>
        <p>{{ contact.phone }}</p>
      </div>

      <div>
        <h2>Connect</h2>
        <div class="social-links">
          <a href="#facebook">Facebook</a>
          <a href="#instagram">Instagram</a>
          <a href="#youtube">YouTube</a>
        </div>
      </div>
    </div>

    <p class="copyright">© 2026 JOCRE University. All rights reserved.</p>
  </footer>
</template>

<style scoped>
.site-footer {
  padding: 34px 30px 20px;
  background: #f8f4ec;
  border-top: 1px solid #e6dcc9;
  color: #352b27;
}

.footer-grid {
  max-width: 1280px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: 1.4fr repeat(3, 1fr);
  gap: 32px;
}

.footer-eyebrow,
.site-footer h2 {
  margin: 0 0 13px;
  font-weight: 700;
}

.footer-eyebrow {
  color: #780e1c;
  font-size: 15px;
}

.site-footer h2 {
  font-size: 14px;
}

.footer-copy,
.site-footer p,
.footer-links,
.social-links {
  color: #65594e;
  font-size: 14px;
  line-height: 1.7;
}

.site-footer p {
  margin: 4px 0;
}

.footer-links,
.social-links {
  display: flex;
  flex-direction: column;
  gap: 4px;
}

.site-footer a {
  color: inherit;
  text-decoration: none;
}

.site-footer a:hover {
  color: #780e1c;
}

.copyright {
  max-width: 1280px;
  margin: 36px auto 0 !important;
  padding-top: 18px;
  border-top: 1px solid #e3d8c7;
  font-size: 12px !important;
}

@media (max-width: 760px) {
  .site-footer {
    padding: 36px 24px 20px;
  }

  .footer-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 480px) {
  .footer-grid {
    grid-template-columns: 1fr;
  }
}
</style>
