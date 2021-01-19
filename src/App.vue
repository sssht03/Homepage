<template>
  <v-app id="app">
    <Main></Main>
  </v-app>
</template>

<script>
import Main from "./components/Main";

export default {
  name: "App",

  components: {
    Main,
  },

  data: () => ({}),
};
</script>

<style>
#app {
  white-space: pre-line;
  width: 100vw;
  margin: 0px;
  padding: 0px;
}
</style>
