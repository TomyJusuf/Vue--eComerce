<template>
  <nav v-bind:style="nav">
    <div v-bind:style="navbar">
      <div v-bind:style="logo">Logo</div>
      <div class="cross" v-on:click="switchBar = !switchBar">
        <div class="a"></div>
      </div>
      <div v-bind:style="info" v-bind:class="[togleClass]">
        <li v-for="item in items" :key="item">{{ item.navbar }}</li>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: "navbarTemplate",
  props: {
    msg: String,
  },
  data() {
    return {
      switchBar: false,
      items: [
        { navbar: "Home" },
        { navbar: "Info" },
        { navbar: "Galery" },
        { navbar: "SHop" },
        { navbar: "Contact" },
      ],
      nav: {
        margin: "0px 10px",
      },
      navbar: {
        display: "flex",
        padding: "10px",
        alignItems: "center",
        justifyContent: "space-between",
        fontSize: "25px",
        flexWrap: "wrap",
      },
      logo: {
        display: "inline-block",
      },
      info: {
        display: "flex",
        justifyContent: " center",
        alignItems: "center",
      },
    };
  },
  computed: {
    togleClass() {
      return {
        close: this.switchBar,
      };
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
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
  }
  navbar {
    align-items: center;
    row-gap: 5px;
  }
  .log {
    margin: 0 auto 10px;
    width: 450px;
    height: 50px;
    padding-top: 5px;
  }

  .info {
    width: 350px;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    margin: 0 auto;
    row-gap: 5px;
    align-content: center;
  }
  .close {
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
</style>
