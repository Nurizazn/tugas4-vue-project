<template>
  <div id="app">
    <ClickCounter />
    <BoxColorChanger />
    <ImageCarousel />
  </div>
</template>

<script>
import ClickCounter from './components/ClickCounter.vue';
import BoxColorChanger from './components/BoxColorChanger.vue';
import ImageCarousel from './components/ImageCarousel.vue';

export default {
  name: 'App',
  components: {
    ClickCounter,
    BoxColorChanger,
    ImageCarousel
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  margin-top: 60px;
}
</style>
