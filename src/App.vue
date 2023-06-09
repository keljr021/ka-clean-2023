<template>
  <!-- <Navbar @scroll-to="scrollTo" /> -->
  <Cta @scroll-to="scrollTo" />
  <Services @scroll-to="scrollTo" />
  <About @scroll-to="scrollTo"/>
  <Contact @scroll-to="scrollTo"/>
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
  methods: {
    scrollTo(input) {
      let el = document.getElementsByClassName(input)[0];
      if(el) el.scrollIntoView({ behavior: 'smooth', inline: 'start' });
    }
  },
  mounted() {
    let input = null;
    if (input)
      this.scrollTo(input);
  },
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

<style lang="scss">
div, p {
  line-height: 2em;
}

.page-section {
  min-height: 500px;
  padding: 50px 0;
  background: #F6F6F6;
}

.page-section-title {
  font-size: 24px;
}

.page-section-subtitle {
  font-size: 18px;
}
</style>
