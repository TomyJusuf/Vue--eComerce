<template>
  <nav>
    <div class="navbar">
      <div class="log">Logo</div>
      <div class="cross" v-on:click="switchBar = !switchBar">
        <div class="a"></div>
      </div>
      <div class="info" :class="togleClass">
        <li v-for="item in items" :key="item">{{ item }}</li>
      </div>
    </div>
  </nav>
</template>

<script>
// import { log } from "console";
import cardSection from "./CardSection.vue";
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  data() {
    return {
      switchBar: false,
      count: cardSection.data(),
      items: ["home", "Info", "Galery", "Shop"],
    };
  },
  computed: {
    togleClass() {
      return {
        close: this.switchBar,
      };
    },
  },
  // components: { CardSection },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
nav {
  margin: 0px auto;
  width: 100%;
  background-color: #61a4e7;
}
.navbar {
  display: flex;
  padding: 10px;
  align-items: center;
  justify-content: space-between;
  font-size: 25px;
  flex-wrap: wrap;
}
.log {
  display: inline-block;
  margin-left: 5%;
}
.info {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-right: 5%;
}
li {
  width: 90px;
  height: 100%;
  margin: 10px 10px;
  list-style-type: none;
}

@media (max-width: 650px) {
  .cross {
    position: absolute;
    width: 50px;
    height: 50px;
    top: 1%;
    left: 88%;
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    cursor: pointer;
    /* transition: all 0.4s ease-in-out; */
  }

  .a {
    position: absolute;
    width: 20px;
    height: 3px;
    margin-left: 20px;
    background-color: #000;
    color: #000;
    transition: all 0.4s ease-in;
  }
  .a::before {
    content: "";
    width: 10px;
    height: 1px;
    padding: 1px;
    background-color: black;
    color: #000;
    position: absolute;
    margin-top: 10px;
    margin-left: -2px;
    transition: all 0.4s ease-in-out;
  }
  .a::after {
    margin-left: -25px;
    position: absolute;
    margin-top: -10px;
    content: "";
    width: 32px;
    height: 1px;
    padding: 1px;
    background-color: black;
    color: #000;
    transition: all 0.4s ease-in-out;
  }

  .cross:hover .a {
    position: absolute;
    width: 0px;
    height: 3px;
    margin-left: 10px;
    background-color: #000;
    color: #000;
  }
  .cross:hover .a::after {
    width: 20px;
    position: absolute;
    margin-top: 1px;
    transform: rotate(140deg);
    margin-left: -2px;
    background-color: #000;
  }
  .cross:hover .a::before {
    position: absolute;
    margin-top: 0px;
    width: 20px;
    margin-left: -2px;
    transform: rotate(-140deg);
    background-color: #000;
  }

  nav {
    height: 100%;
    flex-wrap: wrap;
    display: flex;
    justify-content: center;
  }
  navbar {
    justify-content: center;
    align-items: center;
    row-gap: 5px;
  }
  .log {
    display: block;
    margin: 0 20% 10px;
    width: 400px;
    height: 50px;
    padding-top: 5px;
  }

  .info {
    width: 350px;
    display: flex;
    flex-wrap: wrap;
    margin: 0 auto;
    row-gap: 5px;
    align-content: center;
  }
  .close {
    transition: 1.7s ease-in-out;
    display: none;
  }

  li {
    /* display: none; */
    display: block;
    align-items: center;
    padding-top: 5px;
    margin: 1px auto;
    min-width: 350px;
    height: 50px;
    border-bottom-width: 1px;
    border-bottom-style: solid;
    text-transform: uppercase;
  }
}
.fa-cart-shopping {
  position: absolute;
  margin-left: 440px;
  margin-top: -10px;
  z-index: 20;
  color: yellow;
  font-size: 15px;
  padding: 6px;
  color: #000;
  border-radius: 5px;
  background-color: #fff;
  /* z-index: -1; */
  /* background-color: blue; */
}
.fa-cart-shopping::before {
  position: absolute;
  margin-top: 12px;
  right: 5px;
  font-size: 25px;
  color: red;
  transform: rotate(25deg);
}
</style>
