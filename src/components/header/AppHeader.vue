<template>
    <v-app-bar
        app
        dark
        flat
        color="green"
    >
        <v-toolbar-title>Projeto Curso Vue</v-toolbar-title>
        <v-spacer />
        <v-toolbar-items>
            <v-btn text>
                Livros
            </v-btn>
            <v-btn text>
                Minha Coleção
            </v-btn>
            <v-btn text>
                Sair
            </v-btn>
        </v-toolbar-items>
    </v-app-bar>
</template>

<script>
    export default {
        name: 'AppHeader',
    };
</script>
