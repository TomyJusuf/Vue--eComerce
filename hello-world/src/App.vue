<template>
  <div>{{ greet }} {{ name }}</div>
  <div v-html="element"></div>
  <div v-text="channel"></div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      greet: "Hello",
      name: "Tomas",
      channel: "Rassass",
      element: "<b>Texting html element</b>",
    };
  },
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
</style>
