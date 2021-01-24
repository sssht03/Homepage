<template>
  <h1 class="section-title py-8 text-center">{{ title }}</h1>
</template>

<script>
export default {
  props: ["title"],
};
</script>

<style>
.section-title {
  color: #f25f4c;
  font-size: 5rem;
}
</style>