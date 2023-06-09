<template>
    <div class="menu">
       <div class="menu-box" @click="toggleMenu">
            <div class="closed" v-if="openMenu">Closed</div>
            <div class="open" v-else>Open</div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'FixedMenu',
    data() {
        return {
            openMenu: false 
        }
    },
    methods: {
        toggleMenu() {
            this.openMenu = !this.openMenu;
        }
    }
}
</script>

<style scoped lang="scss">
.menu {
    position: fixed;
    right: 0;
    bottom: 55px;
    width: 200px;
    background: #666;
    cursor: pointer;
    z-index: 1;


    .menu-box {
        z-index: 1;
        .open, .closed {
            width: 5px;
            color: black
        }
    }
}
</style>