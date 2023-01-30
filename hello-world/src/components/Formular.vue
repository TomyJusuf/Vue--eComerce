<template>
  <div>
    <pre>
      {{ JSON.stringify(formValues, null, 5) }}
    </pre>
  </div>
  <div class="formular">
    <form action="" @submit="submitForm">
      <h2>Travel Information</h2>
      <div class="form-name">
        <label class="firstName" for="firstName">First Name: </label>
        <input type="text" name="firstName" id="firstName" required />
        <label for="lastName">Last Name: </label>
        <input type="text" name="lastName" id="lastName" required />
        <label for="date">Date</label>
        <input type="date" id="date" name="date" />
      </div>

      <div class="form-example">
        <label class="email" for="email">E-mail </label>
        <input type="text" name="email" id="email" required />
        <label class="phoneNumber" for="phoneNumber">Phone Number </label>
        <input type="text" name="phoneNumber" id="phoneNumber" required />
      </div>

      <div class="form-adrese">
        <label class="adress" for="adress">Address 1</label>
        <input type="text" name="address" id="address" required />
      </div>

      <div class="form-adrese">
        <label class="adress-2" for="adress">Address 2</label>
        <input type="text" name="address" id="address" required />
      </div>

      <div class="form-city">
        <label class="city" for="city">City</label>
        <input type="text" name="city" id="city" required />

        <label for="state" class="state">State / Province</label>
        <input type="text" name="state" id="state" required />
        <label for="country" class="country">Country</label>
        <select name="country" id="country">
          <option value="volvo">Paris</option>
          <option value="volvo">New zeland</option>
          <option value="volvo">Maui</option>
          <option value="volvo">Bora Bora</option>
          <option value="volvo">Tahity</option>
          <option value="volvo">London</option>
          <option value="volvo">Holand</option>
          <option value="volvo">Kanada</option>
          <option value="volvo">USA</option>
          <option value="volvo">Swizerland</option>
          <option value="volvo">Austria</option>
          <option value="volvo">Czech Republic</option>
          <option value="volvo">Italia</option>
        </select>
        <label for="zipCode" class="zipCode">Postal / Zip Code</label>
        <input type="text" name="zipCode" id="zipCode" required />
      </div>
      <hr style="margin: 35px 0" />

      <h2>Travel Details</h2>
      <div class="travelDetails">
        <label for="dateDetail">Travel Date</label>
        <input type="date" id="dateDetail" name="date" />
      </div>
      <div class="destination">
        <label for="destination">Destination</label>
        <input type="text" id="destination" name="destination" />
      </div>
      <hr style="margin: 35px 0" />

      <h2>Type of Trip</h2>
      <div class="type-of-trip">
        <label for="honeymoon">Honeymoon</label>
        <input type="radio" id="honeymoon" name="honeymoon" value="honeymoon" />
        <label for="business">Business</label>
        <input type="radio" id="business" name="business" value="business" />
        <label for="familyVocation">Family Volation</label>
        <input
          type="radio"
          id="familyVocation"
          name="familyVocation"
          value="familyVocation"
        />
        <label for="other">Other</label>
        <input type="radio" id="other" name="other" value="other" />
      </div>
      <h2>Other Services Needed</h2>
      <div class="type-of-trip">
        <label for="Flights">Flights Only</label>
        <input type="radio" id="Flights" name="Flights" value="Flights" />
        <label for="rental-car">Rental Car</label>
        <input
          type="radio"
          id="rental-car"
          name="rental-car"
          value="rental-car"
        />
        <label for="entertainment">entertainment</label>
        <input
          type="radio"
          id="entertainment"
          name="entertainment"
          value="entertainment"
        />
        <label for="Hotel">Hotel / Resorts</label>
        <input type="radio" id="Hotel" name="Hotel" value="Hotel" />
      </div>
      <hr style="margin: 35px 0" />
      <h2>Credit Card</h2>
      <div class="travelDetails">
        <input
          type="text"
          id="creaditCard"
          name="firstNameCard"
          placeholder="Enter card number"
        />
      </div>
    </form>
  </div>
</template>

<script>
export default {
  name: "FormTable",
  data() {
    return {
      formValues: {
        firstNname: "",
        lastName: "",
        date: "",
        eMail: "",
        phoneNumber: "",
        adreseStreet: "",
        city: "",
        state: "",
        zipCode: "",
        country: [],
      },
    };
  },
  methods: {
    submitForm(even) {
      event.preventDefault();
      console.log("form values", this.formValues);
    },
  },
};
</script>

<style scoped>
.formular {
  width: 800px;
  display: flex;
  margin: 0 auto;
  background-color: rgb(240, 232, 232);
}
form {
  width: 750px;
  margin: 10px auto;
}
label + input {
  margin: 0 20px;
}

.form-name,
.form-example,
.form-adrese,
.form-city,
.travelDetails,
.destination {
  background-color: #fff;
  margin: 15px 0;
}
#firstName,
#lastName {
  width: 110px;
  height: 30px;
}
#date {
  margin-left: 25px;
  width: 170px;
}
.firstName {
  margin-right: 2px;
}
#email,
#phoneNumber,
#address,
#city,
#state,
#zipCode,
#country,
#dateDetail,
#destination {
  height: 30px;
}
.form-name > label:nth-of-type(3) {
  margin-left: 0px;
}

.email {
  margin-right: 40px;
}
.phoneNumber {
  margin-left: 100px;
  margin-right: 15px;
}
#phoneNumber {
  margin-left: 1px;
}
.adress {
  margin-right: 21px;
}
.adress-2 {
  margin-right: 18px;
}
#address {
  width: 610px;
}
#date {
  width: 180px;
  height: 30px;
}

.form-city > #state {
  width: 250px;
  margin-top: 5px;
  margin-bottom: 5px;
}
.state {
  margin-left: 105px;
}
.zipCode {
  margin-left: 168px;
}
#zipCode {
  width: 170px;
}

.city {
  margin-right: 65px;
}
#country {
  margin-left: 52px;
}
.form-city #city,
.form-city #state {
  width: 170px;
}
#creaditCard {
  width: 110px;
  height: 30px;
}
</style>
