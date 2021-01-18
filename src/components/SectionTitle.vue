<template>
  <h1 class="section-title py-8">{{ title }}</h1>
</template>

<script>
export default {
  props: ["title"],
};
</script>

<style>
.section-title {
  color: #a7a9be;
  font-size: 5rem;
  text-align: center;
}
</style>
