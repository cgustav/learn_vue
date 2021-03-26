<template>
  <h1>CarOptions.vue</h1>
  <hr />
  <h2>Coche - Options API</h2>
  <p>Marca: {{ brand }}</p>
  <p>Modelo: {{ model }}</p>
  <p>Potencia: {{ power }}</p>

  <button @click="upPower(10)">Aumentar</button>
  <button @click="downPower(10)">Disminuir</button>
</template>

<script>
export default {
  // Options API version 2.x
  data() {
    return {
      brand: "Seat",
      model: "Leon",
      power: 50,
    };
  },

  methods: {
    upPower(newPower) {
      this.power += newPower;
    },
    downPower(newPower) {
      this.power -= newPower;
    },
  },
};
</script>

<style></style>
