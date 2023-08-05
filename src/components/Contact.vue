<template>
    <div class="page-section contact">
        <v-container>
       <v-row>
            <v-col class="page-section-title py-6">Contact</v-col>
        </v-row>

        <v-lazy
                :min-height="200"
                :options="{ 'threshold': 0.75 }"
                transition="scroll-y-reverse-transition">
            <v-row>
                <v-col cols="12" sm="6" md="6" lg="6">
                    <p class="py-3">Three ways to contact us:</p>

                    <v-row class="py-3">
                        <v-col cols="1" class="text-center" v-if="$vuetify.display.lgAndUp"><v-icon>fas fa-mobile-screen-button</v-icon></v-col>
                        <v-col cols="10" offset="1">
                            <b>Call or Text Us: </b><br />
                            <a href="tel:9106335896">(910) 633-5896</a>
                        </v-col>
                    </v-row>
                    <v-row class="py-3">
                        <v-col cols="1" class="text-center" v-if="$vuetify.display.lgAndUp"><v-icon>fas fa-envelope</v-icon></v-col>
                        <v-col cols="10" offset="1">
                            <b>Email Us: </b><br />
                            <a href="mailto:kaclean2020@gmail.com">kaclean2020@gmail.com</a>
                        </v-col>
                    </v-row>
                    <v-row class="py-3">
                        <v-col cols="1" class="text-center" v-if="$vuetify.display.lgAndUp"><v-icon>fas fa-file-lines</v-icon></v-col>
                        <v-col cols="10" offset="1">
                            Fill out our <b>Contact Form </b><br />
                            <div class="py-8">
                                <v-btn color="#464DA0" :size="$vuetify.display.lgAndUp ? 'large' : 'default'" ripple @click="this.$emit('openForm')">
                                    <v-icon class="px-5">fas fa-file-lines</v-icon>
                                    Open Contact Form
                                </v-btn>
                            </div>
                        </v-col>
                    </v-row>
                </v-col>
                <v-col cols="12" sm="6" md="6" lg="6">
                    <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d52291.98938979519!2d-78.41395588257573!3d35.00046309206618!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x89ab9dad3039c625%3A0x6d127f6703ecac5f!2sClinton%2C%20NC%2028328!5e0!3m2!1sen!2sus!4v1686265527391!5m2!1sen!2sus" width="100%" height="450" style="border:0;" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
                </v-col>
            </v-row>
        </v-lazy>
        </v-container>
    </div>
</template>

<script>
export default {
    name: 'Contact',
    emits: [
        'openForm'
    ]
}
</script>

<style scoped lang="scss">
.contact {
    a {
        color: black;
    }

    :deep(.v-btn) {
        color: white;
    }
    
    iframe {
        width: 100%;
    }
}
</style>