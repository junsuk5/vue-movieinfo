<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <product />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import Product from "./components/Product.vue";
import Card from "./components/Card.vue";

export default {
  name: "app",
  components: {
    HelloWorld,
    Product,
    Card
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
