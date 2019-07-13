<template>
  <div id="TranslateIn">
    Translation
    <form v-on:submit="formSubmit">
      <input type="text" v-model="textToTranslate" placeholder="Write the text to translate"/>
      <input type="submit" value="Translate">
    </form>
  </div>
</template>

<script>
export default {
  name: "TranslateIn",
  data() {
    return {
      textToTranslate: "",
      languaje: ""
    };
  },
  created() {
    this.languaje = "en";
  },
  methods: {
    formSubmit(e) {
      this.$emit("formSubmit", this.textToTranslate, this.languaje);
      e.preventDefault();
    }
  }
};
</script>

<style>
</style>

