<template>
  <h1>CarComposition.vue</h1>
  <hr />
  <h2>Coche - Composition API</h2>
  <p>Marca: {{ brand }}</p>
  <p>Modelo: {{ model }}</p>
  <p>Potencia: {{ power }}</p>
  <button @click="upPower(10)">Aumentar</button>
  <button @click="downPower(10)">Disminuir</button>
</template>

<script>
import { ref } from "vue";
export default {
  setup() {
    const brand = "Audi";
    const model = "A4";
    let power = ref(30);

    const upPower = (newPower) => {
      power.value += newPower;
    };
    const downPower = (newPower) => {
      power.value -= newPower;
    };

    return {
      brand,
      model,
      power,
      upPower,
      downPower,
    };
  },
};
</script>

<style></style>
