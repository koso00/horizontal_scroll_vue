<template>
  <div class="sticky">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: "StickyInnerContainer",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.sticky {
  position: sticky;
  top: 0;
  height: 100vh;
  width: 100%;
  overflow-x: hidden;
}
</style>
