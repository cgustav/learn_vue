<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld msg="Welcome to Your Vue.js App" /> -->
  <h1>Vue JS</h1>
  <Car />
  <CarComposition />
  <CarOptions />
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";
import Car from "./components/Car.vue";
import CarComposition from "./components/CarComposition.vue";
import CarOptions from "./components/CarOptions.vue";

export default {
  components: {
    Car,
    CarComposition,
    CarOptions,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
}
</style>
