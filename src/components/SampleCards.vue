<template>
  <div class="card">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: "SampleCards",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.card {
  position: relative;
  height: 300px;
  width: 500px;
  background-color: #111f30;
  margin-right: 75px;
  flex-shrink: 0;
}
</style>
