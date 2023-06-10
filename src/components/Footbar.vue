<template>
    <div class="footbar py-1 my-0 px-5">
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
    font-size: 12px;
    color: #999;

    a {
        text-decoration: none;
        color: #999;

        &:hover {
            color: #ccc;
        }
    }
}
</style>