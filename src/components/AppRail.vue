<!--
Az AppRail a main ablak bal széle mentén az AppHeadertől AppFooterig végighúzódó
egyoszlopos ikonsáv. Az ikonok (gombok) egy felső és egy alsó slotban
helyezkednek el. Az ikonok számát és a main ablak minimális magasságát úgy kell
megválasztani, hogy a scrollbar ne jelenjen meg.
-->

<template>
    <v-navigation-drawer class="app-rail" rail permanent>
        <template #prepend>
            <v-list density="compact" nav>
                <v-list-item v-for="( [icon, to, title], idx ) of upperItems" :prepend-icon="icon" :to="to"
                    :title="title" :key="idx"
                    :class="{ 'mb-0': idx === upperItems.length - 1, 'v-list-item--active': to !== '/' && $route.path.startsWith(to) }" />
            </v-list>
        </template>

        <template #append>
            <v-list density="compact" nav>
                <v-list-item v-for="( [icon, to, title], idx ) of lowerItems" :prepend-icon="icon" :to="to"
                    :title="title" :key="idx" :class="{ 'mb-0': idx === lowerItems.length - 1 }" />
            </v-list>
        </template>
    </v-navigation-drawer>
</template>


<script>
    export default {
        data: () => ({
            activeItem1: null,
            activeItem2: null
        }),

        created() {
            this.upperItems = [
                ['mdi-file-document-multiple-outline', '/', "My Files"],
                ['mdi-magnify', '/subpage-1', "Title 2"],
                ['mdi-source-branch', '/b', "Title 3"],
                ['mdi-bug-play-outline', '/subpage-3', "Title 4"]
            ];

            this.lowerItems = [
                ['mdi-account-circle-outline', '/profile', "Title 3"],
                ['mdi-cog', '/settings', "Title 4"]
            ];
        }
    };
</script>


<style scoped>
    .app-rail {}
</style>
