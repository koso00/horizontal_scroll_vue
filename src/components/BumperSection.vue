<template>
  <div class="bumper">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: "BumperSection",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.bumper {
  text-align: center;
  padding: 128px 16px;
  background-color: #efefef;
}
</style>
