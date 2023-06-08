<template>
    <div class="page-section" id="cta">
        <v-container>
            <v-col cols="6" offset="3">
                <div class="cta-logo py-4">
                    <img src="../assets/logo-white.png" alt="K&A Morrisey Cleaning Services" />
                </div>
                <div class="cta-text text-center">
                    <p class="py-2">We're a family-owned business of professional cleaning technicians. With over twenty years experience, K&A Morrisey Cleaning Services have the expertise on all commercial cleaning needs.</p>
                    <p class="py-2">There are no jobs too big or too small!</p>
                </div>
                <div class="cta-links text-center">
                    <div>Services</div>
                    <div>Areas We Serve</div>
                    <div>About</div>
                </div>
            </v-col>
        </v-container>
    </div>
</template>

<script>
export default {
    name: 'Cta'
}
</script>

<style scoped lang="scss">
.page-section {
    background: #999;
}

.cta {
    p {
        line-height: 1.25;
    }
    .cta-logo img {
        height: 150px;
    }
}
</style>