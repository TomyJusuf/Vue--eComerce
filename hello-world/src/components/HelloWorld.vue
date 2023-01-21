<template>
  <nav>
    <div class="navbar">
      <div class="log">Logo</div>
      <div class="cross">
        <div class="a"></div>
      </div>
      <div class="info">
        <li>Home</li>
        <li>Info</li>
        <li>Galery</li>
        <li>Shop</li>
        <li>Contact</li>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
nav {
  margin: 0px 10px;
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
}
.info {
  display: flex;
  justify-content: center;
  align-items: center;
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
    background-color: #fff;
    top: 1%;
    left: 88%;
    display: flex;
    flex-wrap: wrap;
    align-items: center;
  }
  .a {
    width: 40px;
    height: 1px;
    padding: 1px;
    background-color: #000;
    color: #000;
  }
  .a::before {
    content: "";
    width: 10px;
    height: 1px;
    padding: 1px;
    background-color: #000;
    color: #000;
    position: absolute;
    margin-top: 10px;
  }
  .a::after {
    position: absolute;
    margin-top: -10px;
    content: "";
    width: 40px;
    height: 1px;
    padding: 1px;
    background-color: #000;
    color: #000;
  }
  nav {
    height: 100%;
    /* background: red; */
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
  li {
    /* display: none; */
    display: block;
    align-items: center;
    padding-top: 5px;
    margin: 1px auto;
    min-width: 350px;
    height: 50px;
    /* text-decoration: underline; */
    border-bottom-width: 1px;
    border-bottom-style: solid;
    text-transform: uppercase;
  }
}
</style>
