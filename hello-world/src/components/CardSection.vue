<template>
  <link
    rel="stylesheet"
    href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.2.1/css/all.min.css"
    integrity="sha512-MV7K8+y+gLIBoVD59lQIYicR65iaqukzvf/nwasF0nqhPay5w/9lJmVM2hMDcnK1OnMGCdVK+iQrJ7lzPJQd1w=="
    crossorigin="anonymous"
    referrerpolicy="no-referrer"
  />
  <div class="container-card">
    <h1>Make trip <br />The Best destination in world.</h1>
    <div class="border-card">
      <div class="card" v-for="card in cards" :key="card">
        <i class="fa-solid fa-cart-shopping">{{ this.count }}</i>
        <div class="picture-box">
          <img v-bind:src="card.image" class="imagePicture" img />
        </div>
        <div class="title">
          <h2>{{ card.nameDestination }}</h2>
        </div>
        <br />
        <div class="icons-bar">
          <i class="fa-solid fa-star"></i>
          <i class="fa-solid fa-star"></i>
          <i class="fa-solid fa-star"></i>
        </div>
        <h4 class="order">{{ card.start }} - {{ card.end }}</h4>
        <!-- <h3 class="visit">Visit</h3> -->
        <div class="price-border">
          Price:
          <i class="fa-solid fa-plus" v-on:click="increment(1)"></i>
          <div class="price">{{ card.price }}e</div>
          <i class="fa-solid fa-minus" v-on:click="decrement(1)"></i>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardSection",
  data() {
    return {
      message: "hallo there",
      cards: [
        {
          nameDestination: "Paris",
          price: 500,
          picture: "image",
          start: "Fr, 10.may",
          end: "Di, 14.may",
          image:
            "https://static.independent.co.uk/s3fs-public/thumbnails/image/2020/04/14/17/istock-958597180.jpg?quality=75&width=982&height=726&auto=webp",
        },
        {
          nameDestination: "New Zealand",
          price: 600,
          picture: "image",
          start: "Fr, 10.may",
          end: "Di, 14.may",
          image:
            "https://www.twowanderingsoles.com/wp-content/uploads/2021/07/img_60ee7d07ab465.jpg",
        },
        {
          nameDestination: "Maui",
          price: 900,
          picture: "image",
          start: "Fr, 10.may",
          end: "Di, 14.may",
          image:
            "https://www.travelandleisure.com/thmb/Zc6w093C6a7OlsANt7aOeqAjXTU=/1500x0/filters:no_upscale():max_bytes(150000):strip_icc()/maui-hawaii-MAUITG0221-50725a14980e4a3382eab85f50339099.jpg",
        },
        {
          nameDestination: "Bora Bora",
          price: 1500,
          picture: "image",
          start: "Fr, 10.may",
          end: "Di, 14.may",
          image:
            "https://media.triseptsolutions.com/sites/vaxwebuav/PublishingImages/UV_destinations/dest_BOB_thumb2.jpg",
        },
        {
          nameDestination: "Tahiti",
          price: 3500,
          picture: "image",
          start: "Fr, 10.may",
          end: "Di, 14.may",
          image:
            "https://pictures.tripmasters.com/images/packages1/french_polynesia/frenchpolynesia-tahiti-bungalow500.jpg",
        },
        {
          nameDestination: "London",
          price: 2500,
          picture: "image",
          start: "Fr, 10.may",
          end: "Di, 14.may",
          image:
            "https://image.urlaubspiraten.de/720/image/upload/v1603987364/mediavault_images/big_ben_london_city_trip_lk35rm.png",
        },
        {
          nameDestination: "Holand",
          price: 1500,
          picture: "image",
          start: "Fr, 10.may",
          end: "Di, 14.may",
          image:
            "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT-Isn9Tpp7lGdr7XG6IOhlGW__MNDK0-n-iA&usqp=CAU",
        },
        {
          nameDestination: "Kanada",
          price: 3500,
          picture: "image",
          start: "Fr, 10.may",
          end: "Di, 14.may",
          image:
            "https://res.cloudinary.com/worldpackers/image/upload/c_fill,f_auto,q_auto,w_1024/v1/guides/article_cover/vae4vwglxryqdd1owwth",
        },
        {
          nameDestination: "USA",
          price: 2500,
          picture: "image",
          start: "Fr, 10.may",
          end: "Di, 14.may",
          image:
            "https://i2-prod.mirror.co.uk/incoming/article23789788.ece/ALTERNATES/n615/1_Young-lady-visiting-Statue-of-Liberty-in-New-York.jpg",
        },
        {
          nameDestination: "Swizerland",
          price: 2500,
          picture: "image",
          start: "Fr, 10.may",
          end: "Di, 14.may",
          image:
            "https://www.myglobalviewpoint.com/wp-content/uploads/2020/01/Most-beautiful-places-in-Switzerland.jpg",
        },

        {
          nameDestination: "Austria",
          price: 1500,
          picture: "image",
          start: "Fr, 10.may",
          end: "Di, 14.may",
          image:
            "https://travelpassionate.com/wp-content/uploads/2019/04/Scenic-view-of-famous-Hallstatt-village-in-the-Austrian-Alps.-Image-min.jpg",
        },
        {
          nameDestination: "Czech Republic",
          price: 3500,
          picture: "image",
          start: "Fr, 10.may",
          end: "Di, 14.may",
          image:
            "https://media.wired.co.uk/photos/606db186a329c00890ec0888/master/w_1600%2Cc_limit/czech-republic-prague.jpg",
        },
        {
          nameDestination: "Italia",
          price: 2500,
          picture: "image",
          start: "Fr, 10.may",
          end: "Di, 14.may",
          image:
            "https://lp-cms-production.imgix.net/features/2017/11/GettyRF_543346423-1-ab159824d5bd.jpg",
        },
      ],
      count: 0,
      number: this.count,
    };
  },
  methods: {
    increment(num) {
      this.count += num;
      console.log(this.count);
      return this.count;
    },
    decrement(num) {
      this.count = this.count - num;
      console.log(this.count);
      return this.count;
    },
  },
};
</script>

<style scoped>
.container-card {
  display: flex;
  flex-wrap: wrap;
  background-color: rgb(190, 225, 226);
  max-width: 1200px;
  height: 99%;
  margin: 50px auto;
  padding: 1px 1px;
  gap: 10px 20px;
  justify-content: center;
  border-radius: 15px;
  /* border: 10px solid red; */
}
.border-card {
  display: flex;
  flex-wrap: wrap;
  background-repeat: no-repeat;
  /* background: linear-gradient(#b9b3eb, #070c41); */
  background: linear-gradient(
      45deg,
      rgba(34, 102, 204, 0.8),
      rgba(233, 133, 133, 0.842) 70.71%
    ),
    /* linear-gradient(145deg, rgba(223, 230, 223, 0.8), rgba(0, 255, 0, 0) 70.71%), */
      linear-gradient(
        45deg,
        rgba(4, 5, 59, 0.534),
        rgba(169, 206, 240, 0.904) 70.71%
      );
  border: 15px solid white;
  max-width: 1110px;
  height: 100%;
  margin: 15px auto 30px;
  padding: 10px 10px;
  gap: 10px 20px;
  justify-content: center;
  padding-bottom: 10px !important;
  border-radius: 15px;
}

.container-card h1 {
  /* max-width: 1280px; */
  font-size: 2.3rem;
  justify-content: center;
  align-self: flex-start;
  margin-top: 20px;
  position: relative;
  flex-wrap: wrap;
  width: 600px;
  display: block;
  margin-bottom: 10px;
  color: rgb(32, 26, 26);
  text-decoration: underline;
  background-color: rgb(243, 240, 236);
  border-radius: 15px;
}

.border-card .card {
  margin-top: 10px;
  display: flex;
  flex-direction: row;
  flex: 0 250px;
  max-width: 230px;
  height: 300px;
  background-color: rgb(255, 255, 255);
  /* box-shadow: 3px 2px 4px rgb(65, 63, 63); */

  flex-wrap: wrap;
  justify-content: center;
  align-items: flex-start;
  color: black;
  border-radius: 10px 10px 10px 10px;
}
.card > .title {
  font-size: 15px;
  color: black;
  display: block;
  width: 100%;
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
.icons-bar > .fa-solid {
  color: rgb(255, 217, 0);
}
.price-border {
  font-size: 15px;
}
.fa-solid {
  margin: 0 5px;
  cursor: pointer;
}
.price-border > .price {
  display: inline-flex;
  width: 60px;
  height: 20px;
  align-items: center;
  justify-content: center;
  align-self: flex-start;
  border: none;
  /* cursor: pointer; */
  border-radius: 4px;
  color: rgb(26, 21, 21);
  font-size: 15px;
  font-weight: bold;
  margin-left: 5px;
  background-color: cornflowerblue;
}
.border-card > .card:hover {
  position: relative;
  /* scale: 1.2; */
  z-index: 10;
  box-shadow: 5px 5px 4px rgb(65, 63, 63);
  top: -5px;
}
.fa-cart-shopping {
  position: absolute;
  margin-left: 200px;
  margin-top: 220px;
  z-index: 20;
  color: yellow;
  font-size: 15px;
  padding: 6px;
  color: rgb(248, 243, 243);
  border-radius: 5px;
  background-color: rgb(17, 16, 16);
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
