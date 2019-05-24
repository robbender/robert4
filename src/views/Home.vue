<template>
  <div id="app">
  <v-app id="inspire">
    <main id="bg-color" class="w-100 min-vh-100 sans-serif pa6 flex flex-column justify-center items-center">
      <div class="mw8 center overflow-hidden">
        <h2 class="tc ttu tracked3 b f2 mt0 mb2 o-30">vue-fontawesome</h2>

        <ul class="list ma0 pa0 flex flex-row flex-wrap ">
          <li class="pv3 ph2 ma0 link grow">
            <font-awesome-icon icon="coffee" size="4x" />
          </li>
          <li class="pv3 ph2 ma0 link grow">
            <font-awesome-icon :icon="['fas', 'coffee']" flip="horizontal" size="4x" />
          </li>
          <li class="pv3 ph2 ma0 link grow">
            <font-awesome-icon :icon="['far', 'comment']" size="4x" />
          </li>
          <li class="pv3 ph2 ma0 link grow">
            <font-awesome-icon icon="child" transform="shrink-4 down-2 right-2" :mask="['fas', 'circle']" size="4x" />
          </li>
          <li class="pv3 ph2 ma0 link grow">
            <font-awesome-icon :icon="['fab', 'twitter']" size="4x" />
          </li>
          <li class="pv3 ph2 ma0 link grow">
            <font-awesome-layers full-width class="fa-4x">
              <font-awesome-icon :icon="['fas', 'archive']"/>
              <font-awesome-layers-text class="red8" transform="down-3 shrink-14" value="SECRET" />
            </font-awesome-layers>
          </li>
        </ul>
      </div>
    </main>
    </v-app>
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
  /* background-color: #3AAFA9; */
}
#app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    background-color: #3AAFA9;
}
#bg-color {
  background-color: #3AAFA9;
}

#17252A

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
  color: #42b983;
}
</style>

