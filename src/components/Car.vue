<template>
  <div class="content">
    <h2 class="title">Automóvil - Composition</h2>
    <p>Marca: {{ brand }}</p>
    <p>Modelo: {{ model }}</p>
    <p>Potencia: {{ power }}</p>
    <button @click="upPower">Aumentar</button>
    <button @click="downPowerFn">Disminuir</button>
  </div>
</template>

<script>
export default {
  props: {
    power: {
      type: Number,
      default: 60,
    },
    upPower: Function,
  },

  emits: ["downPower"],

  setup(props, context) {
    const brand = "Audi";
    const model = "A4";

    const downPowerFn = () => {
      context.emit("downPower");
    };

    return {
      brand,
      model,
      downPowerFn,
    };
  },
};
</script>

<style lang="scss">
.content {
  background-color: gray;
  .title {
    color: red;
  }
}
</style>
