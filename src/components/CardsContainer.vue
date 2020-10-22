<template>
  <div class="cards">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: "CardsContainer",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.cards {
  position: relative;
  height: 100%;
  padding: 0 0 0 150px;
  display: flex;
  flex-flow: row nowrap;
  justify-content: flex-start;
  align-items: center;
}
</style>
