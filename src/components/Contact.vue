<template>
    <div class="page-section contact">
        <v-container>
       <v-row>
            <v-col class="page-section-title py-6">Contact</v-col>
        </v-row>

        <v-lazy
                :min-height="300"
                :options="{ 'threshold': 0.75 }"
                transition="scroll-y-reverse-transition">
            <v-row>
                <v-col>
                    <p class="py-3">Three ways to contact us:</p>
                    <div class="py-5 pl-2">
                        <v-icon class="pr-5">fas fa-mobile-screen-button</v-icon>
                        <b>Call or Text Us: </b><br />
                        <a  class="pl-10" href="tel:9106335896">(910) 633-5896</a>
                    </div>
                    <div class="py-5 pl-2">
                        <v-icon class="pr-5">fas fa-envelope</v-icon>
                        <b>Email Us: </b><br />
                        <a class="pl-10" href="mailto:kaclean2020@gmail.com">kaclean2020@gmail.com</a>
                    </div>
                    <div class="py-5 pl-2">
                        <v-icon class="pr-5">fas fa-file-lines</v-icon>
                        Fill out our <b>Contact Form </b><br />
                        <div class="py-9">
                            <v-btn color="#464DA0" size="large" ripple @click="this.$emit('openForm')">
                                <v-icon class="px-5">fas fa-file-lines</v-icon>
                                Open Contact Form
                            </v-btn>
                        </div>
                    </div>
                </v-col>
                <v-col>
                    <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d52291.98938979519!2d-78.41395588257573!3d35.00046309206618!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x89ab9dad3039c625%3A0x6d127f6703ecac5f!2sClinton%2C%20NC%2028328!5e0!3m2!1sen!2sus!4v1686265527391!5m2!1sen!2sus" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
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
}

</style>