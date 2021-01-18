<template>
  <v-app-bar fixed color="#72757e">
    <v-spacer></v-spacer>
    <v-toolbar-items class="hidden-sm-and-down">
      <v-btn text v-for="item in contentsList" :key="item">{{ item }}</v-btn>
    </v-toolbar-items>
  </v-app-bar>
</template>

<script>
export default {
  data() {
    return {
      contentsList: ["about", "career", "skills", "product"],
    };
  },
};
</script>

<style>
.appbar {
  color: #010101;
}
</style>
