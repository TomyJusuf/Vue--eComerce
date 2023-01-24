<template>
  <!-- <Navbar />
  <CardSection /> -->
  <template v-for="name in names" :key="name">
    <h2 v-if="name === 'Bruce'">{{ name }}</h2>
  </template>
</template>

<script>
// import Navbar from "./components/Navbar.vue";
// import CardSection from "./components/CardSection.vue";
export default {
  name: "App",
  data() {
    return {
      names: ["Bruce", "Clark", "Diana"],
      fullName: [
        { first: "Bruce", last: "Wayne" },
        { first: "Clark", last: "Kent" },
        { first: "Princess", last: "Diana" },
      ],
      actors: [
        {
          name: "Christian Bale",
          movies: ["Barman", "The Prestige"],
        },
        {
          name: "Di Caprio",
          movies: ["Titanic", "Inceprion"],
        },
      ],
      myInfo: {
        name: "Tomas",
        channel: "Developer",
        couse: "Vue 3",
      },
    };
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
