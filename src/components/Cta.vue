<template>
    <div class="page-section cta">
        <v-container>
            <v-col cols="6" offset="3" class="text-center">
                <div class="cta-logo py-4">
                    <img src="../assets/logo-white.png" alt="K&A Morrisey Cleaning Services" />
                </div>
                <div class="cta-text py-4">
                    <p class="py-2">We're a family-owned business of professional cleaning technicians. With over twenty years experience, K&A Morrisey Cleaning Services have the expertise on all commercial cleaning needs.</p>
                    <p class="py-2">There are no jobs too big or too small!</p>
                </div>
                <div class="cta-links py-8">
                    <v-row class="justify-space-between">
                        <v-col>
                            <div class="text-center px-2" @click="this.$emit('scrollTo', 'services')">Services</div>
                        </v-col>
                        <v-col>
                            <div class="text-center px-2" @click="this.$emit('scrollTo', 'areas')">Areas We Serve</div>
                        </v-col>
                        <v-col>
                            <div class="text-center px-2" @click="this.$emit('scrollTo', 'about')">About</div>
                        </v-col>
                    </v-row>
                </div>
            </v-col>
        </v-container>
    </div>
</template>

<script>
export default {
    name: 'Cta',
    emits: [
        'scrollTo'
    ]
}
</script>

<style scoped lang="scss">
.page-section {
    height: 100vh;
    background: #1D2352;
    color: white;
}

.cta {
    font-size: 1.25em;

    p {
        line-height: 1.25;
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
</style>