<template>
  <h2>Automóvil - Composition</h2>
  <p>Marca: {{ brand }}</p>
  <p>Modelo: {{ model }}</p>
  <p>Potencia: {{ power }}</p>
</template>

<script>
export default {
  props: {
    power: {
      type: Number,
      default: 60,
    },
  },

  setup(props) {
    const brand = "Audi";
    const model = "A4";

    console.log(props);

    return {
      brand,
      model,
    };
  },
};
</script>

<style></style>
