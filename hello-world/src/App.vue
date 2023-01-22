<template>
  <!-- <Navbar /> -->
  <h2 v-bind:id="headingId">Heading</h2>
  <button v-bind:disabled="isDisabled">Bind</button>
  <h2 class="underline">Underline text</h2>
  <h2 v-bind:class="underline">Text</h2>
  <h2
    v-bind:style="{
      background: hightlight,
      fontSize: headerSize + 'px',
    }"
  >
    Inline Style
  </h2>
  <h2 v-bind:style="headerStyleOBject">Style Object</h2>

  <div v-bind:style="[baseStyleObject, successStyleObject]">Success Style</div>
  <div v-bind:style="[baseStyleObject, dangerStyleObject]">Danger Style</div>
</template>

<script>
// import Navbar from "./components/Navbar.vue";
export default {
  name: "App",
  data() {
    return {
      greet: "Hello",
      name: "Tomas",
      channel: "<b>Coco-Logo</b>",
      headingId: "heading",
      isDisabled: true,
      underline: "underline",
      hightlight: "orange",
      headerSize: 50,
      headerStyleOBject: {
        color: "orange",
        fontSize: "50px",
        padding: "20px",
      },
      baseStyleObject: {
        fontSize: "50px",
        padding: "10px",
      },
      successStyleObject: {
        color: "green",
        backgroundColor: "lightgreen",
        border: "1px solid green",
      },
      dangerStyleObject: {
        color: "darkred",
        backgroundColor: "red",
        border: "1px solid darkred",
      },
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
