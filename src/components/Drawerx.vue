<template>
    <v-navigation-drawer mobile-breakpoint="md">
        <v-list v-model:active="activeItem" :lines="false" density="compact" nav slim>
            <v-list-item v-for="([icon, to, title], idx) of menuItems" link :prepend-icon="icon" :to="to" :title="title"
                :key="idx" exact />
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
                ['mdi-home', '/', "h"],
                ['mdi-home', '/fdgdfgfdg', "dfgdfgfdg"]
            ];
        }
    }
</script>
