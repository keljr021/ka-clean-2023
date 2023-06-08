<template>
    <div class="page-section" id="services">
        <v-container fluid>
        Services Here

        <v-row>
            <v-col>
                <ServiceCard />
            </v-col>
            <v-col>
                <ServiceCard />
            </v-col>
            <v-col>
                <ServiceCard />
            </v-col>
        </v-row>
        </v-container>
    </div>
</template>

<script>
import ServiceCard from './ServiceCard.vue'
export default {
    name: 'Services',
    components: {
        ServiceCard
    }
}
</script>

<style scoped lang="scss">
.page-section {
    background: #ccc;
}
</style>