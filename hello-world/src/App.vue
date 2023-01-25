<template>
  <!-- <Navbar /> -->
  <!-- <CardSection /> -->
  <Formular />

  <h1>hi</h1>
</template>

<script>
// import CardSection from "./components/CardSection.vue";
// import Navbar from "./components/Navbar.vue";
import Formular from "./components/Formular.vue";
export default {
  name: "App",
  data() {
    return {};
  },
  methods: {},
  components: { Formular },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@200;300;400;500;600&display=swap");

#app {
  font-family: "Poppins", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: rgb(41, 36, 36);
  /* margin-top: 0px; */
}
</style>
