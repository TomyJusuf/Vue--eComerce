<template>
  <div class="container-card">
    <div class="card" v-for="card in cards" :key="card">
      <div class="title">
        <h2>{{ card.nameDestination }}</h2>
      </div>
      <div class="picture-box">
        <img
          src="image/image1.jpeg"
          alt=""
          srcset=""
          class="imagePicture"
          img
        />
      </div>
      <h3>price: {{ card.price }}$</h3>
      <button>Order now</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardSection",
  data() {
    return {
      cards: [
        {
          nameDestination: "Paris",
          price: 500,
          picture: "image",
        },
        {
          nameDestination: "New Zealand",
          price: 600,
          picture: "image",
        },
        {
          nameDestination: "Maui",
          price: 900,
          picture: "image",
        },
        {
          nameDestination: "Bora Bora",
          price: 1500,
          picture: "image",
        },
        {
          nameDestination: "Tahiti",
          price: 3500,
          picture: "image",
        },
        {
          nameDestination: "London",
          price: 2500,
          picture: "image",
        },
      ],
    };
  },
};
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: row;
  height: 45px;
  justify-content: center;
  align-items: flex-start;
}

.container > ul {
  align-items: center;
  display: flex;
  width: 100%;
  background-color: var(--bg-color);
  list-style-type: none;
  flex-direction: row;
  padding: 10px 30px;
  gap: 20px;
  font-size: 30px;
  font-weight: bold;
}

ul > .log {
  flex: 1;
  justify-content: flex-start;
}

.container-card {
  display: flex;
  flex-wrap: wrap;
  background-color: var(--color);
  max-width: 1050px;
  height: 100%;
  margin: 100px auto;
  padding: 10px 10px;
  gap: 10px 50px;
  justify-content: center;
  padding-bottom: 100px !important;
  border-radius: 15px;
}
.container-card h1 {
  font-size: 70px;
  justify-content: center;
  align-self: flex-start;
  margin-top: 20px;
  position: absolute;
}
p {
  font-size: 20px;
  margin-top: 50px;
  position: relative;
  color: rgb(43, 34, 34);
  text-align: justify;
  width: 550px;
}

.card {
  margin-top: 130px;
  display: flex;
  flex-direction: row;
  flex: 0 250px;
  max-width: 250px;
  height: 400px;
  background-color: var(--bg-color);
  box-shadow: 5px -4px 7px rgb(165, 156, 156);
  flex-wrap: wrap;
  justify-content: center;
  align-items: flex-start;
  color: black;
  border-radius: 15px;
}
.card > .title {
  display: flex;
  font-size: 20px;
  color: black;

  align-items: center;
  margin-top: 15px;
  text-decoration: underline;
}
.card > .picture-box {
  position: relative;
  display: inline-flex;
  flex-direction: column;
  align-self: flex-start;
  border: 3px solid black;
  margin-top: 0px;
  justify-self: center;
  border-radius: 8px;
}
.picture-box img {
  width: 230px;
  height: 150px;
  overflow: hidden;
  border-radius: 7px;
}
.card h3 {
  display: flex;
  width: 100%;
  justify-content: center;
  text-align: center;
  align-self: flex-start;
  margin-top: 70px;
  color: #000;
  font-size: 25px;
  font-weight: bold;
}

.card button {
  display: flex;
  width: 150px;
  height: 30px;
  padding: 0 auto;
  align-items: center;
  justify-content: center;
  align-self: flex-start;
  border: none;
  box-shadow: 5px -4px 7px rgb(90, 84, 84);
  cursor: pointer;
  border-radius: 4px;
  background-color: rgb(226, 224, 200);
  color: rgb(26, 21, 21);
  font-size: 19px;
  font-weight: bold;
}
</style>
