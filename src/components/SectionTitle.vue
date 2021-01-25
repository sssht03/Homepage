<template>
  <div :class="{ fadeIn: show, text: !show }">
    <h1 class="py-8 text-center">
      <slot v-show="this.show">{{ title }}</slot>
    </h1>
  </div>
</template>

<script>
export default {
  props: ["title", "show"],
};
</script>

<style>
.text {
  font-size: 3rem;
  opacity: 0;
}
.fadeIn {
  color: #f25f4c;
  font-size: 3rem;
  animation: fadeIn 1s;
}
@keyframes fadeIn {
  0% {
    opacity: 0;
    transform: translateX(-15rem);
  }
  100% {
    opacity: 1;
    transform: translateX(0px);
  }
}
</style>