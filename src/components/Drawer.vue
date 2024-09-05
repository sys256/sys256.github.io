<template>
    <v-navigation-drawer mobile-breakpoint="md">
        <v-list v-model:active="activeItem" :lines="false" density="compact" nav slim>
            <v-list-item v-for="([icon, to, title], idx) of menuItems" link :prepend-icon="icon" :to="to" :title="title"
                :key="idx" />
        </v-list>
    </v-navigation-drawer>
</template>


<script>
    export default {
        data: () => ({
            activeItem: null
        }),

        created() {
            this.menuItems = [
                ['mdi-home', '/', "Home"],
                ['mdi-home', '/about', "About"],
                ['mdi-home', '/b', "b"],
                ['mdi-home', '/kitchen-sink', "Kitchen Sink"],
                ['mdi-home', '/b/registration', "Registration"],
                ['mdi-home', '/settings', "Settings"],
                ['mdi-home', '/b/subpage-2', "Subpage 2"],
                ['mdi-home', '/dummy-1', "Dummy 1"],
                ['mdi-home', '/dummy-2', "Dummy 2"]
            ];
        }
    }
</script>
