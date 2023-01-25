<template>
  <!-- <Navbar /> -->
  <!-- <CardSection /> -->
  <!-- <Formular /> -->

  <pre>
      {{ JSON.stringify(formValues, null, 5) }}
    </pre
  >

  <form action="" @submit.prevent="submitForm">
    <div>
      <label for="name">Name</label>
      <input type="text" id="name" v-model.trim.lazy="formValues.name" />
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
      <label class="country-label" for="country">Country</label>
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

    <div class="question">
      <label for="remoteWork">Open to remote work?</label>
      <input
        type="checkbox"
        id="remoteWork"
        v-model="formValues.remoteWork"
        true-value="yes"
        false-value="no"
      />
    </div>
    <div class="question">
      <label for="">Skill set :</label>
      <input
        type="checkbox"
        id="html"
        value="html"
        v-model="formValues.skillSet"
      />
      <label for="html">HTML</label>
      <input
        type="checkbox"
        id="css"
        value="css"
        v-model="formValues.skillSet"
      />
      <label for="css">CSS</label>
      <input
        type="checkbox"
        id="javascript"
        value="javascript"
        v-model="formValues.skillSet"
      />
      <label for="javascript">JavaScript</label>
    </div>

    <div class="question">
      <label for="">Years of Experience :</label>
      <input
        type="radio"
        id="0-2"
        value="0-2"
        v-model="formValues.yearOfExperience"
      />
      <label for="html">0-2</label>
      <input
        type="radio"
        id="3-5"
        value="3-5"
        v-model="formValues.yearOfExperience"
      />
      <label for="css">3-5</label>
      <input
        type="radio"
        id="6-10"
        value="6-10"
        v-model="formValues.yearOfExperience"
      />
      <label for="javascript">6-10</label>
    </div>
    <div>
      <label for="age">Age</label>
      <input
        @keyup.enter="submitForm"
        type="number"
        id="age"
        v-model.number="formValues.age"
      />
    </div>

    <!-- <div>
      <button>Submit</button>
    </div> -->
  </form>
</template>

<script>
// import CardSection from "./components/CardSection.vue";
// import Navbar from "./components/Navbar.vue";
// import Formular from "./components/Formular.vue";
export default {
  name: "App",
  data() {
    return {
      formValues: {
        name: "",
        profileSummary: "",
        country: "",
        jobLocation: [],
        remoteWork: "no",
        skillSet: [],
        yearOfExperience: "",
        age: null,
      },
    };
  },
  methods: {
    submitForm() {
      console.log("form values", this.formValues);
    },
  },
  // components: { Formular },
};
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
form {
  display: flex;
  flex-wrap: wrap;
  height: 700px;

  width: 460px;
  margin: 50px auto;
  background-color: cornflowerblue;
  justify-content: center;
  border-radius: 15px;
}
label {
  font-weight: bold;
  display: flex;
  margin-bottom: 1px;
  margin-top: 7px;
}
#country,
#job-location {
  width: 420px;
}
input + label {
  font-weight: bold;
  display: inline-flex;
  /* margin-right: 20px; */
}

.question {
  display: flex;
  width: 100%;
  margin-left: 25px;
}
input[type="text"],
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
}
button {
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
</style>
