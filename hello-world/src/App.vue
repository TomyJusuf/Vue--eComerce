<template>
  <!-- <Navbar /> -->
  <!-- <CardSection /> -->
  <!-- <Formular /> -->

  <h2>fullname- {{ firstName }} {{ lastName }}</h2>
  <h2>Computed fullname- {{ fullName }}</h2>
  <button @click="changeFullName">Change fullName</button>

  <button @click="items.push({ id: 4, title: 'Keyboard', price: 50 })">
    Add item
  </button>
  <h2>Computed total - {{ total }}</h2>
  <h2>Method Total - {{ getTotal() }}</h2>
  <input type="text" v-model="country" />

  <template v-for="item in items" :key="item.id">
    <h2 v-if="item.price > 100">{{ item.title }}{{ item.price }}</h2>
  </template>
  <h2 v-for="item in expensiveItems" :key="item.id">
    {{ item.title }}{{ item.price }}
  </h2>
</template>

<script>
// import CardSection from "./components/CardSection.vue";
// import Navbar from "./components/Navbar.vue";
// import Formular from "./components/Formular.vue";
export default {
  name: "App",
  data() {
    return {
      firstName: "Bruse",
      lastName: "Wayne",
      items: [
        {
          id: 1,
          title: "TV",
          price: 100,
        },
        {
          id: 2,
          title: "Phone",
          price: 200,
        },
        {
          id: 3,
          title: "Laptop",
          price: 300,
        },
      ],
      country: "",
    };
  },
  methods: {
    getTotal() {
      return this.items.reduce(
        (total, current) => (total = total + current.price),
        0
      );
    },
    changeFullName() {
      this.fullName = "Clark Kent 30";
    },
  },
  computed: {
    fullName: {
      get() {
        return `${this.age} ${this.firstName} ${this.lastName} `;
      },
      set(value) {
        const name = value.split(" ");
        this.firstName = name[0];
        this.lastName = name[1];
        this.age = name[2];
      },
    },
    total() {
      return this.items.reduce(
        (total, current) => (total = total + current.price),
        0
      );
    },
    expensiveItems() {
      return this.items.filter((item) => item.price > 100);
    },
  },

  // components: { Navbar, CardSection },
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
  /* text-align: center; */
  color: rgb(41, 36, 36);
  /* margin-top: 0px; */
}
/* form {
  display: flex;
  flex-wrap: wrap;
  height: 700px;

  width: 460px;
  margin: 50px auto;
  background-color: cornflowerblue;
  justify-content: center;
  border-radius: 15px;
} */
/* label {
  font-weight: bold;
  display: flex;
  margin-bottom: 1px;
  margin-top: 7px;
} */
/* #country,
#job-location {
  width: 420px;
} */
/* input + label {
  font-weight: bold;
  display: inline-flex;
} */

/* .question {
  display: flex;
  width: 100%;
  margin-left: 25px;
} */
/* input[type="text"],
textarea,
select {
  display: block;
  width: 400px;
  padding: 6px 12px;
  margin: 0 auto;
  font-size: 14px;
  line-height: 1.428;
  color: #555;
  background-color: #fff;
  border-image: none;
} */
/* button {
  background-color: rgb(87, 172, 8);
  padding: 10px 20px;
  font-size: 20px;
  font-weight: bold;
  border: 3px rgb(238, 220, 220) solid;
  border-radius: 15px;
  color: rgb(240, 248, 248);
  cursor: pointer;
  box-shadow: 4px -1px 5px rgb(66, 54, 54);
}
button:active {
  scale: 0.9;
} */
</style>
