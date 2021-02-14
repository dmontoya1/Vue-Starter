<template>
  <h1>Vue JS</h1>
  <Car :power="power" :upPower="upPower" />
  <hr />
</template>

<script>
import { ref } from "vue";
import Car from "./components/Car";
export default {
  components: {
    Car,
  },
  setup() {
    let power = ref(40);

    const upPower = () => {
      console.log("Aumentar Power ....");
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
