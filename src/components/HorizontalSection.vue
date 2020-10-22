<template>
  <div class="horizontalsection">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: "HorizontalSection",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.horizontalsection {
  position: relative;
  width: 100%;
  min-height: 100vh;
}
</style>
