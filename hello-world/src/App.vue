<template>
  <!-- <Navbar />
  <CardSection /> -->
  <h2>{{ 2 + 3 + 5 }}</h2>
  <h2>Add method - {{ add(5, 10, 15) }}</h2>
  <h2>Multiply method- {{ multiply(baseValue) }}</h2>
</template>

<script>
// import Navbar from "./components/Navbar.vue";
// import CardSection from "./components/CardSection.vue";
export default {
  name: "App",
  data() {
    return {
      names: ["Bruce", "Clark", "Diana"],
      baseMultiplier: 5,
      baseValue: 2,
    };
  },
  methods: {
    add(a, b, c) {
      return a + b + c;
    },
    multiply(num) {
      return num * this.baseMultiplier;
    },
  },

  // components: { CardSection, Navbar },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@200;300;400;500;600&display=swap");
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
#app {
  font-family: "Poppins", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #fff;
  /* margin-top: 0px; */
  background-color: #61a4e7;
}
.underline {
  text-decoration: underline;
}
</style>
