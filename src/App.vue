<template>
  <div id="app">
    <ButterflyMonarch />
  </div>
</template>

<script>
import ButterflyMonarch from "./components/ButterflyMonarch.vue";
import "./assets/css/main.css";

export default {
  name: "App",
  components: {
    ButterflyMonarch,
  },
};
</script>

<style>
#app {
  display: flex;
  flex-direction: column;
}
</style>