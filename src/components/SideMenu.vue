<template>
  <v-container class="sidemenu">
    <v-row v-for="item in contentsList" :key="item" justify="end" class="pa-4"
      ><v-btn text style="color:#fffffe">{{ item }}</v-btn></v-row
    >
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      contentsList: ["About", "Career", "Skills", "Product"],
    };
  },
  components: {},
};
</script>

<style>
.sidemenu {
  height: 15rem;
  position: fixed;
  z-index: 1;
}
</style>
