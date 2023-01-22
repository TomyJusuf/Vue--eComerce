<template>
  <!-- <Navbar /> -->
  <h1 v-if="num === 0">The number is zero</h1>
  <h1 v-else-if="num < 0">The number is negativ</h1>
  <h1 v-else-if="num > 0">The number is positive</h1>
  <h1 v-else>not a number</h1>
</template>

<script>
// import Navbar from "./components/Navbar.vue";
export default {
  name: "App",
  data() {
    return {
      num: 5,
    };
  },
  // components: { Navbar },
};
</script>

<style>
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@200;300;400;500;600&display=swap");
#app {
  font-family: "Poppins", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #fff;
  margin-top: 0px;
  background-color: #61a4e7;
}
.underline {
  text-decoration: underline;
}
</style>
