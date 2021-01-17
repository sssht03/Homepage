<template>
  <v-container>
    <side-menu class="justify-content-end"></side-menu>
    <v-container class="image-background"></v-container>
    <v-container class="main-items">
      <about></about>
      <career></career>
      <!-- <div style="height:2000px"></div> -->
    </v-container>
  </v-container>
</template>

<script>
import About from "./About.vue";
import Career from "./Career.vue";
import SideMenu from "./SideMenu.vue";
export default {
  name: "Main",
  components: { SideMenu, About, Career },

  data: () => ({}),
};
</script>

<style>
.main-container {
  margin-top: 0;
}
.image-background {
  height: 15rem;
  position: fixed;
}
.main-items {
  margin-top: 15rem;
}
</style>
