<template>
    <div class="areas">
        <v-lazy
            :min-height="275"
            :options="{ 'threshold': 0.75 }"
            transition="scroll-y-reverse-transition">
            <v-container>
                <v-row>
                    <v-col class="page-section-title py-6">Areas We Cover</v-col>
                </v-row>
                <v-row>
                    <v-col cols="12" lg="6">
                        <div>
                            <p>K&A Morrisey Cleaning Services are located in <b>Clinton, NC.</b> We provide support to Sampson County and surrounding areas.</p>
                            <p>Not located in our area? Feel free to contact us and one of our cleaning technicians will attempt to support you.</p>
                        </div>
                        <div>
                            <div class="page-section-subtitle pt-12 pb-6">Buildings</div>
                            <div>
                                <v-row>
                                    <v-col>
                                        <ul>
                                            <li>Administrative Offices</li>
                                            <li>Cafeterias</li>
                                            <li>Clerical Offices</li>
                                            <li>Government Facilities</li>
                                            <li>Kitchens</li>
                                        </ul>
                                    </v-col>
                                    <v-col>
                                        <ul>
                                            <li>Libraries</li>
                                            <li>Locker Rooms</li>
                                            <li>Medical Clinics</li>
                                            <li>Meeting Rooms</li>
                                            <li>Restrooms</li>
                                        </ul>
                                    </v-col>
                                </v-row>
                            </div>
                        </div>
                    </v-col>
                    <v-col cols="12" lg="6" class="areas-map">
                        <img src="../assets/north-carolina-county-map-sampson.png" alt="North Carolina Map with Sampson County highlighted" />
                    </v-col>
                </v-row>
            </v-container>
        </v-lazy>
    </div>
</template>

<script>
export default {
    name: 'AreasWeCover'
}
</script>

<style scoped lang="scss">
.areas {
    ul {
        padding-left: 20px;
    }

    li {
        padding-left: 10px;
    }
}

.areas-map img {
    height: 275px;
}

@media all and (max-width: 768px) {
    .areas-map img {
        width: 100%;
        height: auto;
    }
}
</style>