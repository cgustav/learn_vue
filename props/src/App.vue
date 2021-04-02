<template>
  <div>
    <h1>VueJS</h1>
    <Car :power="power" :upPower="upPower" />
  </div>
</template>

<script>
import { ref } from "vue";
import Car from "./components/Car.vue";

export default {
  name: "App",
  components: {
    Car,
  },
  setup() {
    let power = ref(1010);

    const upPower = () => {
      console.log("Aumentando poder...");
      power.value++;
    };

    return {
      power,
      upPower,
    };
  },
};
</script>

<style></style>
