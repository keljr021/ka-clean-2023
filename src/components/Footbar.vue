<template>
    <div class="footbar px-4">
        <div class="text-right">Website provided by <a href="http://kelvin-m.com" target="_blank">Kelvin Morrisey Jr.</a></div>
    </div>
</template>

<script>
export default {
    name: 'Footbar'
}
</script>

<style lang="scss">
.footbar {
    height: 30px;
    background: black;
    color: #666;

    a {
        text-decoration: none;
        color: #666;

        &:hover {
            color: #ccc;
        }
    }
}
</style>