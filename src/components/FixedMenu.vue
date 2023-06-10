<template>
    <div class="menu">
       <div class="menu-box">
            <div class="closed py-0 pl-3 my-1" v-if="openMenu">
                <v-btn-group>
                    <v-btn class="with-border" @click="openLink('tel:9106335896')">
                        <v-icon class="px-5">fas fa-mobile-screen-button</v-icon>
                        (910) 633-5896
                    </v-btn>
                    <v-btn class="with-border" @click="openLink('mailto:kaclean2020@gmail.com')">
                        <v-icon class="px-5">fas fa-envelope</v-icon>
                        kaclean2020@gmail.com
                    </v-btn>
                    <v-btn class="with-border" @click="this.$emit('openForm')">
                        <v-icon class="px-5">fas fa-file-lines</v-icon>
                        Open Contact Form
                    </v-btn>
                    <v-btn @click="toggleMenu">
                        <v-icon class="px-5">fas fa-xmark</v-icon>
                    </v-btn>

                </v-btn-group>
            </div>
            <div class="open pa-3" v-else @click="toggleMenu">
                <v-icon class="px-5">fa-regular fa-comment-dots</v-icon>
                Contact Us
            </div>
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
    emits: [
        'openForm'
    ],
    methods: {
        toggleMenu() {
            this.openMenu = !this.openMenu;
        },
        openLink(link) {
            window.open(link);
        }
    }
}
</script>

<style scoped lang="scss">
.menu {
    position: fixed;
    right: 0;
    bottom: 55px;
    height: 70px;
    cursor: pointer;
    z-index: 1;

    :deep(.v-btn) {
        background-color: transparent !important;
        font-weight: normal;
        text-transform: none;

        &.with-border {
            border-right: 1px solid #333;
        }
    }

    .menu-box {
        border: 1px solid #333;
        border-radius: 20px 0 0 20px;
        border-right: none;
        background: #f6f6f6;
        z-index: 1;

        .open, .closed {
            width: 100%;
            color: black
        }
    }
}
</style>