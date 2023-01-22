<template>
  <Navbar />
  <!-- <h1 v-for="(name, index) in names" :key="name">{{ index }} {{ name }}</h1>
  <div v-for="name in fullName" :key="name">
    <li>{{ name.first }} {{ name.last }}</li>
    <hr />
  </div> -->
  <CardSection />
</template>

<script>
import Navbar from "./components/Navbar.vue";
import CardSection from "./components/CardSection.vue";
export default {
  name: "App",
  data() {
    return {
      names: ["Bruse", "Clark", "Diana"],
      fullName: [
        { first: "Bruce", last: "Wayne" },
        { first: "Clark", last: "Kent" },
        { first: "Princess", last: "Diana" },
      ],
    };
  },
  components: { CardSection, Navbar },
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
  /* background-color: #61a4e7; */
}
.underline {
  text-decoration: underline;
}
</style>
