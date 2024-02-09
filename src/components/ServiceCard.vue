<template>
    <div class="service-card pa-4">
        <div class="service-card-icon py-4">
            <v-icon :icon="'fas fa-' + icon" />
        </div>
        <div class="service-card-title py-2"><b>{{  title }}</b></div>
        <div class="service-card-text">
           {{  text }}
        </div>
    </div>
</template>

<script>
export default {
    name: 'ServiceCard',
    props: {
        icon: String,
        title: String,
        text: String
    }
}
</script>

<style scoped lang="scss">
.service-card-icon {
    font-size: 60px;
    color: #464DA0
}
</style>