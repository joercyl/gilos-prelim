<template>
  <Navbar />
  <RouterView />
  <Footer
    :links="footerLinks"
    :contact="contact"
  />
</template>

<script setup>
import Navbar from './components/NavBar.vue'
import Footer from './components/Footer.vue'

const footerLinks = [
  { label: 'Home', to: '/' },
  { label: 'About', to: '/about' },
  { label: 'Academics', to: '/academics' },
  { label: 'Admissions', to: '/admissions' },
  { label: 'Contact', to: '/contact' }
]

const contact = {
  address: 'JOCRE University Campus, Philippines',
  email: 'admissions@jocreuniversity.edu.ph',
  phone: '+63 900 000 0000'
}
</script>