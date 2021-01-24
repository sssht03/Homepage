<template>
  <v-app-bar fixed color="rgba(114, 117, 126, 0.9)">
    <v-spacer></v-spacer>
    <v-row align-content="end">
      <v-btn
        text
        :x-large="$vuetify.breakpoint.mdAndUp"
        :small="$vuetify.breakpoint.smAndDown"
        v-for="(item, i) in contentsList"
        :key="i"
        :color="item.show ? '#fffffe' : '#000000'"
        >{{ item.title }}</v-btn
      >
    </v-row>
  </v-app-bar>
</template>

<script>
export default {
  data() {
    return {
      contentsList: [
        { title: "about", show: false },
        { title: "career", show: false },
        { title: "skills", show: false },
        { title: "works", show: false },
      ],
    };
  },
};
</script>

<style></style>
