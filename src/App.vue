<template>
    <v-app>
        <app-header />
        <app-footer />

        <app-rail />

        <router-view />
    </v-app>
</template>


<script>
    import AppHeader from '@/components/AppHeader.vue';
    import AppFooter from '@/components/AppFooter.vue';
    import AppRail from '@/components/AppRail.vue';

    export default {
        components: {
            AppHeader,
            AppFooter,
            AppRail
        }
    };
</script>
