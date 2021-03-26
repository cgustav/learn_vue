<template>
  <h1>Car.vue</h1>
  <hr />
  <h2>Coche</h2>
  <p>Marca: {{ brand }}</p>
  <p>Modelo: {{ model }}</p>
  <p>Colores:</p>
  <ul>
    <li v-for="(color, index) in colors" :key="index">
      {{ index }}: {{ color }}
    </li>
  </ul>
  <p>Price: ${{ price }}</p>
  <p>Potencias Urbanas menor a 300 CV (Default)</p>
  <!-- bug version -->

  <ul>
    <li v-for="(power, index) in powers" :key="index">
      <template v-if="power < 300">
        {{ power }}
      </template>
    </li>
  </ul>
  <p>Potencias Urbanas menor a 300 CV (Adapt)</p>
  <!-- adapt version -->

  <ul>
    <template v-for="(power, index) in powers" :key="index">
      <li v-if="power < 300">{{ power }}</li>
    </template>
  </ul>

  <p>Potencias Urbanas Categorizadas (Elsif)</p>
  <!-- elsif version -->

  <ul>
    <template v-for="(power, index) in powers" :key="index">
      <li v-if="power < 280">Urbana: {{ power }}</li>
      <li v-else-if="power === 280">Híbrido: {{ power }}</li>
      <li v-else-if="power > 280">Carrera: {{ power }}</li>

      <li v-if="power === 500">Super: {{ power }}</li>
    </template>
  </ul>
  {{ mensaje.title }} - {{ mensaje.text }}
</template>

<script>
export default {
  // Composition API version 3.x
  setup() {
    const brand = "Audi",
      colors = ["Azul", "Rojo", "Verde"],
      model = "A4",
      price = 38000,
      powers = [60, 80, 120, 160, 200, 280, 300, 390, 540, 500],
      mensaje = {
        title: "Hola mundo",
        text: "Adios",
      };

    return {
      brand,
      model,
      colors,
      price,
      powers,
      mensaje,
    };
  },
};
</script>

<style></style>
