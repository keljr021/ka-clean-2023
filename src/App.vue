<template>
  <!-- <Navbar /> -->
  <Cta />
  <Services />
  <About />
  <Contact />
  <Footbar />
</template>

<script>
import Navbar from './components/Navbar.vue'
import Cta from './components/Cta.vue'
import Services from './components/Services.vue'
import About from './components/About.vue'
import Contact from './components/Contact.vue'
import Footbar from './components/Footbar.vue'
export default {
  name: 'app',
  components: {
    Navbar,
    Cta,
    Services,
    About,
    Contact,
    Footbar
  }
}
</script>

<style>
.page-section {
  min-height: 500px;
}
</style>
