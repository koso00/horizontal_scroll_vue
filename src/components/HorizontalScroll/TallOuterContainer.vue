<template>
  <div class="tall" :style="{ height: `${dynamicHeight}px` }">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: "TallOuterContainer",
  props: ["dynamicHeight"],
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.tall {
  position: relative;
  width: 100%;
}
</style>
