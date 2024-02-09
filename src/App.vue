<template>
    <Navbar @scroll-to="scrollTo" />
    <Cta @scroll-to="scrollTo" />
    <Services />
    <About />
    <Contact @scroll-to="scrollTo" @open-form="openContactForm"/>
    <Footbar />
    <FixedMenu @open-form="openContactForm" />

    <v-dialog v-model="openContactModal" width="80vw" scrollable persistent>
        <v-card>
          <v-container>
            <v-row class="justify-space-between">
              <v-col class="text-right">
                <v-btn fab flat href="https://docs.google.com/forms/d/e/1FAIpQLScwGjQDZYL1k9-IUAPa-XeUbgPFyN-u5_vPcvbOh9i0HeH8XA/viewform?usp=pp_url" target="_blank">
                  <v-icon>fa-solid fa-up-right-from-square</v-icon>
                  <v-tooltip
                    activator="parent"
                    location="bottom">
                      Open Form in new window
                  </v-tooltip>
                </v-btn>
                <v-btn fab flat @click="openContactModal = false">
                  <v-icon>fas fa-xmark</v-icon>
                  <v-tooltip
                    activator="parent"
                    location="bottom">
                      Close Form
                  </v-tooltip>
                </v-btn>
              </v-col>
            </v-row>
          </v-container>

          <v-card-text>
            <div class="py-3 text-center">
              <iframe src="https://docs.google.com/forms/d/e/1FAIpQLSc24Cj9SKgc6MBJKPGraEFBsiimAHjIG25WsnqJUjXdGMxXvw/viewform?embedded=true" width="900" height="1600" frameborder="0" marginheight="0" marginwidth="0">Loading…</iframe>
            </div>
          </v-card-text>
        </v-card>
    </v-dialog>
</template>

<script>
import Navbar from './components/Navbar.vue'
import Cta from './components/Cta.vue'
import Services from './components/Services.vue'
import About from './components/About.vue'
import Contact from './components/Contact.vue'
import Footbar from './components/Footbar.vue'
import FixedMenu from './components/FixedMenu.vue'

export default {
  name: 'app',
  data() {
    return {
      openContactModal: false
    }
  },
  methods: {
    scrollTo(input) {
      let el = document.getElementsByClassName(input)[0];
      if(el) el.scrollIntoView({ behavior: 'smooth', inline: 'start' });
    },
    openContactForm() {
      let onMobileOrTablet = this.$vuetify.display.mdAndDown;
      if (onMobileOrTablet) {
        this.openContactModal = false;
        window.open('https://forms.gle/XRK5Ac1xRLuowPrS7','_blank')
      }
      else {
        this.openContactModal = true;
      }
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
    Footbar,
    FixedMenu
  }
}
</script>

<style lang="scss">
div, p {
  line-height: 2em;
}

.page-section {
  padding: 50px 0;
  background: #F6F6F6;
  z-index: 1;
}

.page-section-title {
  font-family: 'Carlito', 'Roboto', sans-serif;
  font-size: 30px;
}

.page-section-subtitle {
  font-size: 24px;
}
</style>
