<template>
    <div class="page-section contact">
        <v-container>
       <v-row>
            <v-col class="page-section-title py-6">Contact</v-col>
        </v-row>

        <v-row>
            <v-col>
                <p class="py-3">Three ways to contact us:</p>
                <div class="py-5">
                    <b>Call or Text Us: </b><br />
                    <a href="tel:9106335896">(910) 633-5896</a>
                </div>
                <div class="py-5">
                    <b>Email Us: </b><br />
                    <a href="mailto:kaclean2020@gmail.com">kaclean2020@gmail.com</a>
                </div>
                <div class="py-5">
                    Fill out our <b>Contact Form </b><br />
                    
                    <div class="py-3">
                        <v-btn>
                            Open Contact Form
                        </v-btn>
                    </div>
                </div>
            </v-col>
            <v-col>
                <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d52291.98938979519!2d-78.41395588257573!3d35.00046309206618!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x89ab9dad3039c625%3A0x6d127f6703ecac5f!2sClinton%2C%20NC%2028328!5e0!3m2!1sen!2sus!4v1686265527391!5m2!1sen!2sus" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
            </v-col>
        </v-row>
        </v-container>
    </div>
</template>

<script>
export default {
    name: 'Contact'
}
</script>

<style scoped lang="scss">
.contact {
    background: #333;
    color: white;

    a {
        color: white;
    }
}

</style>