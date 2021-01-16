<template>
  <v-container class="sidebar">
    <v-row v-for="item in contensList" :key="item" justify="end" class="pa-4"
      ><v-btn text>{{ item }}</v-btn></v-row
    >
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      contensList: ["About", "Carrer", "Skills", "Product"],
    };
  },
};
</script>

<style>
.sidebar {
  position: fixed;
}
</style>
