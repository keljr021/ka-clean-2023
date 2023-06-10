<template>
    <img class="cta-background" :src="getBg()" alt="cta" />
    <div class="page-section cta">
        <v-container>
            <v-row>
                <v-col class="text-center" cols="12" lg="10" offset-lg="2">
                    <div class="cta-logo py-4">
                        <img src="../assets/logo-white.png" alt="K&A Morrisey Cleaning Services" />
                    </div>
                    <div class="cta-text py-4">
                        <p class="py-2">We're a family-owned business of professional cleaning technicians. With over twenty years experience, K&A Morrisey Cleaning Services have the expertise on all commercial cleaning needs.</p>
                        <p class="py-2">There are no jobs too big or too small!</p>
                    </div>
                    <div class="cta-links py-8 pl-2" v-if="this.$vuetify.display.lgAndUp">
                        <v-row class="justify-space-between">
                            <v-col cols="12" lg="4">
                                <div class="text-center px-2" @click="this.$emit('scrollTo', 'services')">Services</div>
                            </v-col>
                            <v-col cols="12" lg="4">
                                <div class="text-center px-2" @click="this.$emit('scrollTo', 'areas')">Areas We Serve</div>
                            </v-col>
                            <v-col cols="12" lg="4">
                                <div class="text-center px-2" @click="this.$emit('scrollTo', 'about')">About</div>
                            </v-col>
                        </v-row>
                    </div>
                </v-col>
            </v-row>
        </v-container>
    </div>
</template>

<script>
export default {
    name: 'Cta',
    emits: [
        'scrollTo'
    ],
    methods: {
        getBg() {
            return new URL('../assets/desk-cleaning.jpg', import.meta.url).href;
        }
    }
}
</script>

<style scoped lang="scss">
.page-section {
    padding-top: 20px;
    padding-bottom: 80px;
    padding-left: 0;
    padding-right: 0;
    color: white;
}

.cta-background {
    position: fixed;
    right: 0;
    bottom: 0;
    width: 100%;
    object-fit: contain;
    overflow: hidden;
    z-index: -1;
}

.cta {
    position: relative;
    height: 100%;
    background: rgba(29, 35, 82, 0.65);
    -webkit-border-radius: 0;
    border-radius: 0;
    font-family: 'Carlito', 'Roboto', sans-serif;
    font-size: 24px;
    z-index: 0;

    p {
        line-height: 55px;
    }

    .cta-logo img {
        height: 125px;
    }

    .cta-text p {
        line-height: 2.25;
    }

    .cta-links div {
        text-decoration: underline;
        cursor: pointer;
    }
}

@media all and (max-width: 768px) {
    .page-section {
        padding: 20px 0;
    }
    .cta{
        .cta-logo img {
            width: calc(100% - 30px);
            height: auto;
        }
    }
}
</style>