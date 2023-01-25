<template>
  <!-- <Navbar /> -->
  <!-- <CardSection /> -->

  <div>
    <pre>
      {{ JSON.stringify(formValues, null, 5) }}
    </pre>
  </div>
  <form action="">
    <div>
      <label for="name">Name</label>
      <input type="text" id="name" v-model="formValues.name" />
    </div>

    <div>
      <label for="profile">Profile Summary</label>
      <textarea
        name=""
        id="profile"
        cols="30"
        rows="10"
        v-model="formValues.profileSummary"
      ></textarea>
    </div>

    <div>
      <label for="country">Country</label>
      <select name="" id="country" v-model="formValues.country">
        <option value="">select country</option>
        <option value="india">India</option>
        <option value="China">China</option>
        <option value="Europa">Europa</option>
        <option value="Africa">Africa</option>
        <option value="USA">USA</option>
      </select>
    </div>

    <div>
      <label for="job-location">Job Location</label>
      <select
        name=""
        id="job-location"
        multiple
        v-model="formValues.jobLocation"
      >
        <option value="india">India</option>
        <option value="China">China</option>
        <option value="Europa">Europa</option>
        <option value="Africa">Africa</option>
        <option value="USA">USA</option>
      </select>
    </div>
  </form>
</template>

<script>
// import CardSection from "./components/CardSection.vue";
// import Navbar from "./components/Navbar.vue";
export default {
  name: "App",
  data() {
    return {
      formValues: {
        name: "",
        profileSummary: "",
        country: "",
        jobLocation: [],
      },
    };
  },
  methods: {},
};
// components: { Navbar, CardSection },
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@200;300;400;500;600&display=swap");

#app {
  font-family: "Poppins", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: rgb(41, 36, 36);
  /* margin-top: 0px; */
}

label {
  font-weight: bold;
  display: flex;
  margin-bottom: 5px;
}
input + label {
  font-weight: bold;
  display: inline-flex;
  margin-right: 20px;
}
input[type="text"],
textarea,
select {
  display: block;
  width: 400px;
  padding: 6px 12px;
  font-size: 14px;
  line-height: 1.428;
  color: #555;
  background-color: #fff;
  border-image: none;
}
</style>
