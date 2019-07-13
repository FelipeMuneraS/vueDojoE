<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <h1>Traductor</h1>
    <TranslateIn v-on:formSubmit="translate"></TranslateIn>
  </div>
</template>

<script>
import TranslateIn from "./components/TranslateIn.vue";
export default {
  name: "app",
  components: {
    TranslateIn
  },
  methods: {
    translate: function(languaje, text) {
      this.$http
        .get(
          `https://translate.yandex.net/api/v1.5/tr.json/translate?key=trnsl.1.1.20190622T213455Z.f67e95598c7aee64.c0c49d0594aa527178d83c8e3c1a81ed05709a56&lang=${languaje}&text=${text}`)
          .then(Response => {
          this.translate = Response.body.text[0];
        });
    }
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
