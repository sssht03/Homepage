<template>
  <v-row class="products flex-column" justify="center">
    <v-col>
      <section-title :title="'Products'"></section-title>
    </v-col>
    <v-col class="subtitle">
      <v-col>
        <h1>In Progress</h1>
      </v-col>
      <v-col>
        <h1>Past Works</h1>
      </v-col>
    </v-col>
  </v-row>
</template>

<script>
import SectionTitle from "./SectionTitle.vue";
export default {
  data() {
    return {
      inprogress: [
        { title: "", desc: "", skill: "" },
        { title: "", desc: "", skill: "" },
        { title: "", desc: "", skill: "" },
      ],
      pastworks: [
        { title: "", desc: "", skill: "" },
        { title: "", desc: "", skill: "" },
        { title: "", desc: "", skill: "" },
        { title: "", desc: "", skill: "" },
        { title: "", desc: "", skill: "" },
        { title: "", desc: "", skill: "" },
      ],
    };
  },
  components: { SectionTitle },
};
</script>

<style>
.products {
  background-color: #16161a;
}

.subtitle {
  color: #f25f4c;
  font-size: 1.2rem;
  text-align: center;
}
</style>