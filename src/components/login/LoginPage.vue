<template>
    <div>
        <v-container fluid>
            <v-row justify="center">
                <v-col
                    cols="12"
                    md="4"
                    lg="3"
                    class="text-center"
                >
                    <h6 class="display-1 text-uppercase">Login</h6>
                    <v-text-field
                        v-model="token"
                        label="Token"
                    />
                    <v-btn
                        depressed
                        dark
                        block
                        color="green"
                        class="mb-2"
                        @click="login"
                    >
                        Login
                    </v-btn>

                    <v-btn
                        text
                        color="blue"
                        block
                        @click="loginAsGuest"
                    >
                        Entrar como visitante
                    </v-btn>
                </v-col>
            </v-row>
        </v-container>
    </div>
</template>

<script>
/*
            Key Api google Books: AIzaSyBbcvG8W1JLYuY9xTYtYhclegV1xGMeZXE
    */
    export default {
        name: 'LoginPage',
        data() {
            return {
                token: '',
                message: '',
                showMessage: false,
            };
        },
        methods: {
            login() {
                if (this.token) {
                    this.$store.commit('setAuthToken', this.token);
                    this.$router.push('/book');
                } else {
                    this.$store.commit('showErrorMessage', 'Informe o token para continuar');
                    // this.showMessage = true;
                }
            },
            loginAsGuest() {
                // TODO
                this.$router.push('/book');
            },
        },
    };
</script>

<style scoped>

</style>
