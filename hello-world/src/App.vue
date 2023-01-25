<template>
  <Navbar />
  <CardSection />
  <!-- <h2>{{ name }}</h2>
  <div>
    <button v-on:mouseover="name = 'Batman'">Change name</button>
  </div>
  <h2>{{ count }}</h2>
  <div>
    <button v-on:click="increment(10)" @click="method1(multiPly)">
      increment
    </button>
    <button v-on:click="decrement(10)" @click="method2(devide)">
      decrement
    </button>
  </div>
  <div @click="handler1(multiPly)">Hi, click me!</div>
  <div @click="handler(devide)">Hi, click me!</div> -->
</template>

<script>
import CardSection from "./components/CardSection.vue";
import Navbar from "./components/Navbar.vue";
export default {
  name: "App",
  data() {
    return {
      name: "Tomas",
      count: 0,
      multiPly: 150,
      devide: 150,
      count2: 0,
    };
  },
  // methods: {
  //   increment(num) {
  //     this.count += num;
  //   },
  //   decrement(num) {
  //     this.count -= num;
  //   },
  //   method1: function (arg) {
  //     console.log((this.count2 += arg));
  //   },
  //   method2: function (arg) {
  //     console.log((this.count2 -= arg));
  //   },
  // },
  components: { Navbar, CardSection },
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
  background-color: #094683;
}
.underline {
  text-decoration: underline;
}
</style>
