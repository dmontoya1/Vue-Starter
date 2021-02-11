<template>
  <h2>Automóvil - Options</h2>
  <p>Marca: {{ brand }}</p>
  <p>Modelo: {{ model }}</p>
  <p>Potencia: {{ power }}</p>

  <button @click="upPower">Aumentar</button>
  <button @click="downPower">Disminuir</button>
</template>

<script>
export default {
  data() {
    return {
      brand: "Ford",
      model: "Fiesta",
      power: 160,
    };
  },
  methods: {
    upPower() {
      this.power += 1;
    },
    downPower() {
      this.power -= 1;
    },
  },
};
</script>

<style></style>
