<template>
    <div class="navbar">

        <!-- Mobile Navigation -->
        <div class="nav w-100" :class="{'show': showNav }" v-if="$vuetify.display.mobile">
            <v-row class="align-center pl-2 pr-4">
                <v-col cols="9" class="nav-logo" @click="this.$emit('scrollTo', 'cta')">
                    <img src="../assets/logo-color.png" alt="K&A Morrisey Cleaning Services" />
                </v-col>
                <v-col cols="3" class="text-right">
                    <v-btn size="large" id="menu" flat>
                        <v-icon class="text-right">fa-solid fa-bars</v-icon>
                    </v-btn>
                    <v-menu activator="#menu" transition="slide-x-reverse-transition">
                        <v-list>
                            <v-list-item @click="this.$emit('scrollTo', 'services')">Services</v-list-item>
                            <v-list-item @click="this.$emit('scrollTo', 'areas')">Areas We Cover</v-list-item>
                            <v-list-item @click="this.$emit('scrollTo', 'about')">About</v-list-item>
                            <v-list-item @click="this.$emit('scrollTo', 'contact')">Contact</v-list-item>
                        </v-list>
                    </v-menu>
                   
                </v-col>
            </v-row>


        </div>

        <!-- Tablet/Desktop navigation -->
        <div class="nav w-100" :class="{'show': showNav }" v-else>
            <v-row class="align-center">
                <v-col cols="3" class="nav-logo" @click="this.$emit('scroll-to', 'cta')">
                    <img src="../assets/logo-color.png" alt="K&A Morrisey Cleaning Services" />
                </v-col>
                <v-col cols="9" class="text-right">
                    <span class="nav-item" @click.stop="this.$emit('scrollTo', 'services')">Services</span>
                    <span class="nav-item" @click.stop="this.$emit('scrollTo', 'areas')">Areas We Cover</span>
                    <span class="nav-item" @click.stop="this.$emit('scrollTo', 'about')">About</span>
                    <span class="nav-item" @click.stop="this.$emit('scrollTo', 'contact')">Contact</span>
                </v-col>
            </v-row>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Navbar',
    data() {
        return {
            showNav: false
        };
    },
    emits: [
        'scrollTo'
    ],
    methods: {
        checkToShowNavbar() {
            // Get the current scroll position
            const currentScrollPosition = window.pageYOffset || document.documentElement.scrollTop;

            // Because of momentum scrolling on mobiles, we shouldn't continue if it is less than zero
            if (currentScrollPosition < 0) 
            return false;

            // Here we determine whether we need to show or hide the navbar
            this.showNav = currentScrollPosition >= 600;    
       }
    },
    mounted() {
        if (!this.$vuetify.display.mobile) {
            this.checkToShowNavbar();
            window.addEventListener('scroll', this.checkToShowNavbar)
        } else {
            this.showNav = true;
        }
    },
    beforeUnmount () {
        if (!this.$vuetify.display.mobile)
            window.removeEventListener('scroll', this.checkToShowNavbar)
    },
}
</script>

<style lang="scss">
.nav {
    background:white;
    position: fixed;
    z-index: 9999;
    top: -70px;
    transition: top 0.3s;

    &.show {
        top: 0 !important;
    }
}

.nav-logo {
    padding: 0 20px !important;
    cursor: pointer;

    img {
        height: 55px;
        margin: 10px 0;
    }
}

.nav-item {
    padding: 0 20px;
    opacity: 0.8;
    cursor: pointer;

    &:hover {
       opacity: 1;
    }
}

@media all and (max-width: 768px) {
    .nav-logo {
        padding-left: 5px;
        padding-right: 5px;
    }
}
</style>