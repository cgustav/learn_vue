<template>
  <div>
    <h2>Coche - Composition API</h2>
    <p>Marca: {{ brand }}</p>
    <p>Modelo: {{ model }}</p>
    <p>Potencia: {{ power }}</p>
    <button @click="increasePower">Aumentar</button>
    <!-- <p>Potencia: {{ power }}</p> -->
  </div>
</template>

<script>
// import { ref } from "vue";
export default {
  props: {
    power: {
      type: Number,
      default: 60,
    },
    upPower: Function,
  },
  setup(props) {
    const brand = "Audi";
    const model = "A4";

    console.log("Component props: ", props.power);
    // let power = ref(40);

    const increasePower = () => {
      // power.value += newPower;
      props.upPower();
    };

    // const downPower = (newPower) => {
    //   power.value -= newPower;
    // };

    return {
      brand,
      model,
      increasePower,
      // power,
      // upPower,
      // downPower,
    };
  },
};
</script>

<style></style>
