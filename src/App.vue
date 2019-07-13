<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <h1>Traductor</h1>
    <TranslateIn v-on:formSubmit="textToTranslate"></TranslateIn>
  </div>
</template>

<script>
import TranslateIn from "./components/TranslateIn.vue";
export default {
  name: "app",
  components: {
    TranslateIn
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
