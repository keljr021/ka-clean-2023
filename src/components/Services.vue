<template>
    <div class="page-section services">
        <v-container>
            <v-row>
                <v-col class="page-section-title py-6">Services</v-col>
            </v-row>
            <v-lazy
                :min-height="700"
                :options="{ 'threshold': 0.75 }"
                transition="scroll-y-reverse-transition">
                <v-row class="justify-space-between text-center">
                    <v-col cols="4">
                        <ServiceCard 
                            icon="broom" 
                            title="Floors" 
                            text="Waxing, stripping, polishing, cleaning, dry and wet mopping, sweeping, spot removal" 
                        />
                    </v-col>
                    <v-col cols="4">
                        <ServiceCard 
                            icon="rug" 
                            title="Carpets" 
                            text="Cleaning, vacuuming, sweeping, spot removal" 
                        />
                    </v-col>
                    <v-col cols="4">
                        <ServiceCard 
                            icon="building" 
                            title="Offices" 
                            text="Window spot cleaning, dusting, table polishing" 
                        />
                    </v-col>
                    <v-col cols="4">
                        <ServiceCard 
                            icon="mug-saucer" 
                            title="Kitchens" 
                            text="Dishwashing, table cleaning, kitchen appliance cleaning" 
                        />
                    </v-col>
                    <v-col cols="4">
                        <ServiceCard 
                            icon="sink" 
                            title="Restrooms" 
                            text="Toilet cleaning, sink cleaning, disinfecting, tissue refills, soap refills" 
                        />
                    </v-col>
                    <v-col cols="4">
                        <ServiceCard 
                            icon="dumpster" 
                            title="Janitorial" 
                            text="Daily and weekly cleaning, trash removal, debris cleanup" 
                        />
                    </v-col>
                </v-row>
                <v-row>
                    <v-col cols="4" offset="4" class="py-8 page-border">&nbsp;</v-col>
                </v-row>
            </v-lazy>
            <areas-we-cover />
        </v-container>
    </div>
</template>

<script>
import ServiceCard from './ServiceCard.vue'
import AreasWeCover from './AreasWeCover.vue';
export default {
    name: 'Services',
    components: {
        ServiceCard,
        AreasWeCover
    }
}
</script>

<style scoped lang="scss">
.services {
    background: #F6F6F6;

    .page-border {
        border-top: none;
        border-right: none;
        border-bottom: 1px solid #666;
        border-left: none;
    }
}
</style>