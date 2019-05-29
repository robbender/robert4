<template>
<div class="design">
  <v-container id="app">
    <v-layout
      text-xs-center
      wrap
    >
      <v-flex xs12>
        <main class="w-100 min-vh-100 sans-serif pa6 flex flex-column justify-center items-center">
      <div class="mw8 center overflow-hidden">
        <h2 class="tc ttu tracked3 b f2 mt0 mb2 o-1">About Robert</h2>

        <ul class="list ma0 pa0 flex flex-row flex-wrap teal4">
          <li class="pv3 ph2 ma0 link grow">
            <a href=""><font-awesome-icon :icon="['fas', 'code']" transform="shrink-4 down-0 left-0" :mask="['fas', 'circle']" size="4x" @click="code" /></a>
          </li>
          
          <li class="pv3 ph2 ma0 link grow">
            <a href="" target="_blank"><font-awesome-icon :icon="['fas', 'id-badge']" size="4x" /></a>
          </li>
          <li class="pv3 ph2 ma0 link grow">
            <a href="https://github.com/robbender" target="_blank"><font-awesome-icon :icon="['fab', 'github']" size="4x" /></a>
          </li>
          <li class="pv3 ph2 ma0 link grow">
            <a href="https://www.linkedin.com/in/robert-bender-b152257/" target="_blank"><font-awesome-icon :icon="['fab', 'linkedin']" size="4x" /></a>
          </li>
        </ul>
      </div>
    </main>
      </v-flex>
    </v-layout>
  </v-container>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
export default {
  name: 'home',
  components: {
    HelloWorld
  }
}
</script>

<style scoped>
body {
  margin: 0;
  padding: 0;
}
.design {
  background-color: #2b7a78;
}

#app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    /* color: #17252A; */
    background-color: #3AAFA9;
}

/* 
#17252A
#2b7a78
#3AAFA9
#def2f1 
*/

h1, h2 {
  font-weight: normal;
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
  color: #17252A;
}
</style>