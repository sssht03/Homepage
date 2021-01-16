<template>
  <v-layout wrap>
    <v-container fluid>
      <v-row v-for="item in contensList" :key="item" justify="end" class="pa-4">
        <v-btn text>{{ item }}</v-btn>
      </v-row>
    </v-container>
  </v-layout>
</template>

<script>
export default {
  data: () => ({
    contensList: ["About", "Carrer", "Skills", "Product"],
  }),
};
</script>

<style></style>
