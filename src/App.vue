<template>
  <div id="app">
    <BumperSection>
      <h2>Scroll down to reach the horizontal scroll section</h2>
    </BumperSection>
    <HorizontalSection>
      <HorizontalScroll>
        <CardsContainer>
          <SampleCards v-for="i in 5" :key="i" />
        </CardsContainer>
      </HorizontalScroll>
    </HorizontalSection>
    <BumperSection>
      <h2>You have left the horizontal horizontal scroll section</h2>
    </BumperSection>
  </div>
</template>

<script>
import BumperSection from "./components/BumperSection";
import HorizontalSection from "./components/HorizontalSection";
import HorizontalScroll from "./components/HorizontalScroll";
import CardsContainer from "./components/CardsContainer";
import SampleCards from "./components/SampleCards";

export default {
  name: "App",
  components: {
    BumperSection,
    HorizontalSection,
    HorizontalScroll,
    CardsContainer,
    SampleCards,
  },
};
</script>

<style>
* {
  box-sizing: border-box;
}

body {
  margin: 0;
  font-family: sans-serif;
}
</style>
