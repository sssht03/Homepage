<template>
  <div>
    <Header></Header>
    <about></about>
    <career></career>
    <skill></skill>
    <products></products>
  </div>
</template>

<script>
import About from "./About.vue";
import Career from "./Career.vue";
import Header from "./Header.vue";
import Products from "./Products.vue";
import Skill from "./Skill.vue";

export default {
  name: "Main",
  components: { About, Career, Skill, Header, Products },
};
</script>
