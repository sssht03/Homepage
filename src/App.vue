<template>
  <v-app id="app">
    <v-main>
      <Main></Main>
    </v-main>
  </v-app>
</template>

<script>
import Main from "./components/Main";

export default {
  name: "App",

  components: {
    Main,
  },

  data: () => ({
    //
  }),
};
</script>

<style>
#app {
  background-color: #16161a;
  color: #fffffe;
}
</style>
