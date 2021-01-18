<template>
  <div>
    <Header></Header>
    <about></about>
    <career></career>
    <skills></skills>
  </div>
</template>

<script>
import About from "./About.vue";
import Career from "./Career.vue";
import Header from "./Header.vue";
import Skills from "./Skills.vue";
export default {
  name: "Main",
  components: { About, Career, Skills, Header },

  data: () => ({}),
};
</script>

<style></style>
