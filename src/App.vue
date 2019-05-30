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

                    <v-list-tile>
                        <v-list-tile-action>
                            <router-link to="/" tag="Home">
                                <v-btn flat icon color="">
                                    <v-icon>home</v-icon>
                                </v-btn>
                            </router-link>
                        </v-list-tile-action>
                        <router-link to="/">Home</router-link>
                    </v-list-tile>

                    <v-list-tile>
                        <v-list-tile-action>
                            <router-link to="/about" tag="About">
                                <v-btn flat icon color="">
                                    <v-icon>person</v-icon>
                                </v-btn>
                            </router-link>
                        </v-list-tile-action>
                        <router-link to="/about">About</router-link>
                    </v-list-tile>

                    <v-list-tile>
                        <v-list-tile-action>
                            <router-link to="/contact" tag="Contact">
                                <v-btn flat icon color="">
                                    <v-icon>contact_mail</v-icon>
                                </v-btn>
                            </router-link>
                        </v-list-tile-action>
                        <router-link to="/contact">Contact</router-link>
                    </v-list-tile>

                    <v-list-tile>
                        <v-list-tile-action>
                            <router-link to="/experience" tag="Experience">
                                <v-btn flat icon color="">
                                    <v-icon>work</v-icon>
                                </v-btn>
                            </router-link>
                        </v-list-tile-action>
                        <router-link to="/experience">Experience</router-link>
                    </v-list-tile>

                </v-list>
            </v-navigation-drawer>
            <v-toolbar app color="#def2f1">
                <v-toolbar-side-icon @click.stop="drawer = !drawer"></v-toolbar-side-icon>
                <v-toolbar-title class="headline text-uppercase">
                    <v-btn class="display-1" flat color="">Robert
                        <span class="font-weight-light">Bender</span></v-btn>
                </v-toolbar-title>
                <v-spacer></v-spacer>
                <v-btn flat href="/home" target="">
                    <span class="mr-2">Contact Me</span>
                </v-btn>
                <v-btn icon>
                    <!-- <v-toolbar-side-icon @click.stop="drawerRight = !drawerRight"></v-toolbar-side-icon> -->
                    <v-icon @click.stop="drawerRight = !drawerRight">more_vert</v-icon>
                </v-btn>
            </v-toolbar>
            <v-content>

            </v-content>
            </v-app>
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
}

body {
    margin: 0;
    padding: 0;
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
    color: #2c3e50;
    text-decoration: none;
    font-weight: bold;
}
</style>
