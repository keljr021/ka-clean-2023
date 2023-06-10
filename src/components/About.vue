<template>
    <div class="page-section about">
        <v-container class="about-text">
            <v-row>
                <v-col class="page-section-title py-6">About</v-col>
            </v-row>
            <v-lazy
                :min-height="275"
                :options="{ 'threshold': 0.75 }"
                transition="scroll-y-reverse-transition">
                <v-row>
                    <v-col>
                        <p class="py-3"><b>Morrisey Cleaning Services</b> was first created by founders Thurman and Linda Morrisey. With their dedication and hard-work, both have garnished a positive reputation for their expertise in the janitorial business for decades.</p>
                        <p class="py-3">Today, their ethics and values were passed down to their son and his wife Kelvin and Amy Morrisey. Along with their hard-working technicians; they are equipped with the experience to take on any commercial cleaning service for their customers.</p>
                    </v-col>
                    <v-col>
                        <div class="page-section-subtitle py-3">Why Choose Us?</div>
                        <ul class="py-3">
                            <li>North Carolina owned business local to Sampson County</li>
                            <li>Over two decades of janitorial experience</li>
                            <li>Equipped to handle any cleaning requirements</li>
                            <li>Reliable cleaning technicians that you can depend on</li>
                            <li>Track record of quick turnaround time</li>
                            <li>Fully-insured cleaning service</li>
                        </ul>
                    </v-col>
                </v-row>
            </v-lazy>
        </v-container>
    </div>
</template>

<script>
export default {
    name: 'About'
}
</script>

<style scoped lang="scss">
.page-section {
    color: white;
}
.about {
    position: relative; 
    width: 100%;
    background-image: url('@/assets/cleaning-supply-wood.jpg');
    background-size: cover;
    background-position: center;
    z-index: 1;
    font-weight: normal;

    &:before {
        content: "";
        position: absolute;
        top: 0px;
        right: 0px;
        bottom: 0px;
        left: 0px;
        background: rgba(29, 35, 82, 0.75);
    }

    .about-text {
        position: relative;
        z-index: 1;
    }

    ul {
        padding-left: 20px;
    }

    li {
        padding-left: 10px;
    }
}
</style>