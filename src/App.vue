<template>
<div id="app">
    <div id="nav">
        <template>
            <v-navigation-drawer fixed v-model="drawerRight" right clipped app>
                <v-list dense>
                    <v-list-tile @click.stop="right = !right">
                        <v-list-tile-action>
                            <v-icon>exit_to_app</v-icon>
                        </v-list-tile-action>
                        <v-list-tile-content>
                            <v-list-tile-title>Open Temporary Drawer</v-list-tile-title>
                        </v-list-tile-content>
                    </v-list-tile>
                </v-list>
            </v-navigation-drawer>
            <v-navigation-drawer v-model="drawer" fixed app>
                <v-list dense>
                    <v-list-tile @click="">
                        <v-list-tile-action>
                            <v-icon>home</v-icon>
                        </v-list-tile-action>
                        <v-list-tile-content>
                            <router-link to="/">Home</router-link>
                            <!-- <v-list-tile-title>Home</v-list-tile-title> -->
                        </v-list-tile-content>
                    </v-list-tile>
                    <v-list-tile @click="">
                        <v-list-tile-action>
                            <v-icon>person</v-icon>
                        </v-list-tile-action>
                        <v-list-tile-content>
                            <router-link to="/about">About</router-link>
                            <!-- <v-list-tile-title>About</v-list-tile-title> -->
                        </v-list-tile-content>
                    </v-list-tile>
                    <v-list-tile @click="">
                        <v-list-tile-action>
                            <v-icon>contact_mail</v-icon>
                        </v-list-tile-action>
                        <v-list-tile-content>
                            <router-link to="/contact">Contact</router-link>
                            <!-- <v-list-tile-title>Contact</v-list-tile-title> -->
                        </v-list-tile-content>
                    </v-list-tile>
                </v-list>
            </v-navigation-drawer>
            <v-toolbar app color="#def2f1">
                <v-toolbar-side-icon @click.stop="drawer = !drawer"></v-toolbar-side-icon>
                <v-toolbar-title class="headline text-uppercase">
                    <span>Robert</span>
                    <span class="font-weight-light">Bender</span>
                </v-toolbar-title>
                <v-spacer></v-spacer>
                <v-btn flat href="https://github.com/vuetifyjs/vuetify/releases/latest" target="_blank">
                    <span class="mr-2">Contact Me</span>
                </v-btn>
                <v-btn icon>
                    <!-- <v-toolbar-side-icon @click.stop="drawerRight = !drawerRight"></v-toolbar-side-icon> -->
                    <v-icon @click.stop="drawerRight = !drawerRight">more_vert</v-icon>
                </v-btn>
            </v-toolbar>
            <v-content>

            </v-content>
        </template>

    </div>
    <router-view />
</div>
</template>

<script>
// import Landing from './components/Landing'
export default {
    name: 'App',
    components: {

    },
    data: () => ({
        drawer: false,
        drawerRight: false,
        right: null,
        left: null
    }),
    props: {
        source: String
    }
}
</script>

<style scoped>
#app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: ;
    
}

body {
    margin: 0;
    padding: 0;
    background-color: #3AAFA9;
}

h3 {
    margin: 40px 0 0;
}

ul {
    list-style-type: none;
    padding: 0;
}

li {
    display: inline-block;
    margin: 0 10px;
}

a {
    color: #42b983;
}
</style>
