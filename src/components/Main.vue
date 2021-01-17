<template>
  <div>
    <selecter></selecter>
    <div class="main-items">
      <about></about>
      <career></career>
      <skills></skills>
    </div>
  </div>
</template>

<script>
import About from "./About.vue";
import Career from "./Career.vue";
import Selecter from "./Selecter.vue";
import Skills from "./Skills.vue";
export default {
  name: "Main",
  components: { About, Career, Skills, Selecter },

  data: () => ({}),
};
</script>

<style>
.main-items {
  padding-top: 13rem;
}
</style>
