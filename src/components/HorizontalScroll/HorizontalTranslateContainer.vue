<template>
  <div class="horizontaltranslate" :style="{ transform: `translateX(${translateX}px)` }">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: "HorizontalTranslateContainer",
  props: ["translateX"],
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.horizontaltranslate {
  position: absolute;
  height: 100%;
  will-change: transform;
}
</style>
