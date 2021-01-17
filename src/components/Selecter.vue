<template>
  <v-container>
    <div class="image-background"></div>
    <v-container class="sidemenu">
      <v-row v-for="item in contentsList" :key="item" justify="end" class="pa-3"
        ><v-btn text style="color: #fffffe">{{ item }}</v-btn></v-row
      >
    </v-container>
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
  height: 13rem;
  position: fixed;
}
.image-background {
  height: 13rem;
  position: fixed;
  background-color: #72757e;
  color: #72757e;
}
</style>
