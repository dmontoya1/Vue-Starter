<template>
  <h2>Automóvil - Composition</h2>
  <p>Marca: {{ brand }}</p>
  <p>Modelo: {{ model }}</p>
  <p>Potencia: {{ power }}</p>

  <button @click="upPower">Aumentar</button>
  <button @click="downPower(20)">Disminuir</button>
</template>

<script>
import { ref } from "vue";
export default {
  setup() {
    const brand = "Audi";
    const model = "A4";
    let power = ref(40);

    const upPower = () => {
      power.value += 1;
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
