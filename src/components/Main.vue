<template>
  <v-container>
    <side-menu></side-menu>
  </v-container>
</template>

<script>
import SideMenu from "./SideMenu.vue";
export default {
  name: "Main",
  components: { SideMenu },

  data: () => ({}),
};
</script>
