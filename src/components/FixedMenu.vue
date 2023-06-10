<template>
    <div class="menu">
        <!-- Mobile menu -->
        <div class="menu-box" v-if="$vuetify.display.mdAndDown">
            <v-menu transition="slide-x-reverse-transition">
                <template v-slot:activator="{ props }">
                    <v-btn v-bind="props" flat>
                        <v-icon class="px-5">fa-regular fa-comment-dots</v-icon>
                    </v-btn>
                </template>
                <v-list>
                    <v-list-item href="tel:9106335896">
                        <v-icon class="px-5">fas fa-mobile-screen-button</v-icon>
                        (910) 633-5896
                    </v-list-item>
                    <v-list-item href="mailto:kaclean2020@gmail.com">
                        <v-icon class="px-5">fas fa-envelope</v-icon>
                        kaclean2020@gmail.com
                    </v-list-item>
                    <v-list-item @click="this.$emit('openForm')">
                        <v-icon class="px-5">fas fa-file-lines</v-icon>
                        Open Contact Form
                    </v-list-item>
                </v-list>
            </v-menu>
        </div>

        <!-- Tablet/Desktop menu -->
        <div class="menu-box" v-else>
           <Transition name="slide-fade" mode="out-in">
                <div v-if="openMenu">
                    <v-btn-group>
                        <v-btn class="with-border" href="tel:9106335896">
                            <v-icon class="px-5">fas fa-mobile-screen-button</v-icon>
                            (910) 633-5896
                        </v-btn>
                        <v-btn class="with-border" href="mailto:kaclean2020@gmail.com">
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
                <div class="open pa-lg-3" v-else>
                    <v-btn flat @click="toggleMenu">
                        <v-icon class="px-5">fa-regular fa-comment-dots</v-icon>
                        <span>Contact Us</span>
                    </v-btn>
                </div>
            </Transition>
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

        .slide-fade-enter-active {
            transition: all 0.2s ease-out;
        }

        .slide-fade-leave-active {
            transition: all 0.2s cubic-bezier(1, 0.5, 0.8, 1);
        }

        .slide-fade-enter-from,
        .slide-fade-leave-to {
            transform: translateX(20px);
            opacity: 0;
        }
    }
}
</style>