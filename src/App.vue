<template>
  <Navbar />
  <LandingPage />
  <Footer />
</template>

<script>
import Navbar from './components/navigation/Navbar.vue'
import LandingPage from './components/LandingPage.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: { Navbar, Footer, LandingPage }
}
</script>

<style>

</style>
