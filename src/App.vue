<template>
    <v-app>
        <Appheader />
        <v-content>
            <router-view />
        </v-content>
        <feedback />
    </v-app>
</template>

<script>
    import Appheader from './components/header/AppHeader.vue';
    import Feedback from './components/feedback/Feedback.vue';

    export default {
        name: 'App',
        components: {
            Feedback,
            Appheader,
        },
        data: () => ({
            //
        }),
    };
</script>
