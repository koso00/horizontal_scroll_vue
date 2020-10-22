<template>
  <TallOuterContainer :dynamicHeight="dynamicHeight">
    <StickyInnerContainer ref="containerRef">
      <HorizontalTranslateContainer :translateX="translateX" ref="objectRef">
        <slot></slot>
      </HorizontalTranslateContainer>
    </StickyInnerContainer>
  </TallOuterContainer>
</template>

<script>
import HorizontalTranslateContainer from "./HorizontalScroll/HorizontalTranslateContainer";
import StickyInnerContainer from "./HorizontalScroll/StickyInnerContainer";
import TallOuterContainer from "./HorizontalScroll/TallOuterContainer";

export default {
  name: "HorizontalScroll",
  data() {
    return {
      dynamicHeight: 0,
      translateX: 0,
    };
  },
  mounted() {
    this.handleDynamicHeight(this.$refs.objectRef);
    window.addEventListener("resize", this.resizeHandler);
    this.applyScrollListener(this.$refs.containerRef);
  },
  methods: {
    applyScrollListener(ref) {
      console.log(ref);
      window.addEventListener("scroll", () => {
        this.translateX = -ref.$el.offsetTop;
      });
    },
    resizeHandler() {
      this.handleDynamicHeight(this.$refs.objectRef);
    },
    handleDynamicHeight(ref) {
      const objectWidth = ref.$el.scrollWidth;
      this.dynamicHeight = this.calcDynamicHeight(objectWidth);
    },
    calcDynamicHeight(objectWidth) {
      const vw = window.innerWidth;
      const vh = window.innerHeight;
      return objectWidth - vw + vh + 150;
    },
  },
  components: {
    HorizontalTranslateContainer,
    StickyInnerContainer,
    TallOuterContainer,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.root {
  position: relative;
  height: 100%;
  padding: 0 0 0 150px;
  display: flex;
  flex-flow: row nowrap;
  justify-content: flex-start;
  align-items: center;
}
</style>
