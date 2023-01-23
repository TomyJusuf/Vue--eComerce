<template>
  <div class="container-card">
    <div class="border-card">
      <h1>Make trip to The Best destination in world.</h1>

      <div class="card" v-for="card in cards" :key="card">
        <div class="picture-box">
          <img
            src="https://media.istockphoto.com/id/1299265795/photo/family-vacation-holiday-happy-family-running-on-the-beach-in-the-sunset-back-view-of-a-happy.jpg?s=612x612&w=0&k=20&c=LQHDTNEzba2gMcpjXCNuRrwIV6Yi3nYvJiomJYuU6No="
            alt=""
            srcset=""
            class="imagePicture"
            img
          />
        </div>
        <div class="title">
          <h2>{{ card.nameDestination }}</h2>
        </div>
        <h4 class="order">{{ card.start }} - {{ card.end }}</h4>
        <!-- <h3 class="visit">Visit</h3> -->
        <h3>
          price: <button>{{ card.price }}e</button>
        </h3>
      </div>
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
          start: "Fr, 10.may",
          end: "Di, 14.may",
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
        {
          nameDestination: "London",
          price: 2500,
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
.container-card {
  display: flex;
  flex-wrap: wrap;
  background-color: rgb(223, 21, 21);
  max-width: 1030px;
  height: 99%;
  margin: 150px auto;
  padding: 1px 1px;
  gap: 10px 20px;
  justify-content: center;
  border-radius: 15px;
}
.border-card {
  display: flex;
  flex-wrap: wrap;
  background-color: rgb(236, 174, 174);
  max-width: 1000px;
  height: 100%;
  margin: 15px auto;
  padding: 10px 10px;
  gap: 10px 20px;
  justify-content: center;
  padding-bottom: 10px !important;
  border-radius: 15px;
}

.border-card h1 {
  max-width: 1080px;
  font-size: 2.3rem;
  justify-content: center;
  align-self: flex-start;
  margin-top: 30px;
  position: relative;
  flex-wrap: wrap;
  width: 100%;
  display: block;
  margin-bottom: 25px;
}

.border-card .card {
  margin-top: 10px;
  display: flex;
  flex-direction: row;
  flex: 0 250px;
  max-width: 230px;
  height: 250px;
  background-color: rgb(217, 217, 231);
  flex-wrap: wrap;
  justify-content: center;
  align-items: flex-start;
  color: black;
  border-radius: 10px 10px 10px 10px;
}
.card > .title {
  font-size: 15px;
  color: black;

  margin-top: 0px;
  text-decoration: underline;
}
.card > .picture-box {
  position: relative;
  display: inline-flex;
  flex-direction: column;
  align-self: flex-start;
  margin-top: 0px;
  justify-self: center;
  border-radius: 8px;
}
.picture-box img {
  width: 230px;
  height: 150px;
  overflow: hidden;
  border-radius: 5px;
  border-radius: 5px 5px 0 0;
}
.card h3 {
  display: inline-block;
  position: relative;
  width: 100%;
  text-align: center;
  align-self: flex-end;
  margin: 0 0px 5px 105px;
  color: #000;
  font-size: 10px;
  font-weight: normal;
}

.card .visit {
  display: inline-block;
  width: 100%;
  margin: 0 auto;
  padding: 0;
  font-size: 15px;
  position: relative;
}
.card .order {
  padding: 0 25px !important;
}

.card h4 {
  font-size: 13px;
}
.card button {
  display: inline-flex;
  width: 60px;
  height: 20px;
  align-items: center;
  justify-content: center;
  align-self: flex-start;
  border: none;
  cursor: pointer;
  border-radius: 4px;
  color: rgb(26, 21, 21);
  font-size: 15px;
  font-weight: bold;
  margin-left: 5px;
}
</style>
