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
        <input
          type="text"
          name="firstName"
          id="firstName"
          v-model="formValues.firstName"
          required
        />
        <label class="lastName" for="lastName">Last Name: </label>
        <input
          type="text"
          name="lastName"
          id="lastName"
          required
          v-model="formValues.lastName"
        />*
        <label class="date" for="date">Date:</label>
        <input type="date" id="date" name="date" v-model="formValues.date" />
      </div>

      <div class="form-example">
        <label class="email" for="email">E-mail: </label>
        <input
          type="text"
          name="email"
          id="email"
          required
          v-model="formValues.eMail"
        />
        <label class="phoneNumber" for="phoneNumber">Phone Number: </label>
        <input
          type="text"
          name="phoneNumber"
          id="phoneNumber"
          required
          v-model="formValues.phoneNumber"
        />
      </div>

      <div class="form-adrese">
        <label class="adress" for="adress">Address 1</label>
        <input
          type="text"
          name="address"
          id="address"
          required
          v-model="formValues.adreseStreet1"
        />
      </div>

      <div class="form-adrese">
        <label class="adress-2" for="adress">Address 2</label>
        <input
          type="text"
          name="address"
          id="address"
          required
          v-model="formValues.adreseStreet2"
        />
      </div>

      <div class="form-city">
        <label class="city" for="city">City</label>
        <input
          type="text"
          name="city"
          id="city"
          required
          v-model="formValues.city"
        />

        <label for="state" class="state">State / Province</label>
        <input
          type="text"
          name="state"
          id="state"
          required
          v-model="formValues.state"
        />
        <label for="country" class="country">Country</label>
        <select id="country" name="country" v-model="formValues.country">
          <option>select country</option>
          <option value="AF">Afghanistan</option>
          <option value="AX">Aland Islands</option>
          <option value="AL">Albania</option>
          <option value="DZ">Algeria</option>
          <option value="AS">American Samoa</option>
          <option value="AD">Andorra</option>
          <option value="AO">Angola</option>
          <option value="AI">Anguilla</option>
          <option value="AQ">Antarctica</option>
          <option value="AG">Antigua and Barbuda</option>
          <option value="AR">Argentina</option>
          <option value="AM">Armenia</option>
          <option value="AW">Aruba</option>
          <option value="AU">Australia</option>
          <option value="AT">Austria</option>
          <option value="AZ">Azerbaijan</option>
          <option value="BS">Bahamas</option>
          <option value="BH">Bahrain</option>
          <option value="BD">Bangladesh</option>
          <option value="BB">Barbados</option>
          <option value="BY">Belarus</option>
          <option value="BE">Belgium</option>
          <option value="BZ">Belize</option>
          <option value="BJ">Benin</option>
          <option value="BM">Bermuda</option>
          <option value="BT">Bhutan</option>
          <option value="BO">Bolivia</option>
          <option value="BQ">Bonaire, Sint Eustatius and Saba</option>
          <option value="BA">Bosnia and Herzegovina</option>
          <option value="BW">Botswana</option>
          <option value="BV">Bouvet Island</option>
          <option value="BR">Brazil</option>
          <option value="IO">British Indian Ocean Territory</option>
          <option value="BN">Brunei Darussalam</option>
          <option value="BG">Bulgaria</option>
          <option value="BF">Burkina Faso</option>
          <option value="BI">Burundi</option>
          <option value="KH">Cambodia</option>
          <option value="CM">Cameroon</option>
          <option value="CA">Canada</option>
          <option value="CV">Cape Verde</option>
          <option value="KY">Cayman Islands</option>
          <option value="CF">Central African Republic</option>
          <option value="TD">Chad</option>
          <option value="CL">Chile</option>
          <option value="CN">China</option>
          <option value="CX">Christmas Island</option>
          <option value="CC">Cocos (Keeling) Islands</option>
          <option value="CO">Colombia</option>
          <option value="KM">Comoros</option>
          <option value="CG">Congo</option>
          <option value="CD">Congo, Democratic Republic of the Congo</option>
          <option value="CK">Cook Islands</option>
          <option value="CR">Costa Rica</option>
          <option value="CI">Cote D'Ivoire</option>
          <option value="HR">Croatia</option>
          <option value="CU">Cuba</option>
          <option value="CW">Curacao</option>
          <option value="CY">Cyprus</option>
          <option value="CZ">Czech Republic</option>
          <option value="DK">Denmark</option>
          <option value="DJ">Djibouti</option>
          <option value="DM">Dominica</option>
          <option value="DO">Dominican Republic</option>
          <option value="EC">Ecuador</option>
          <option value="EG">Egypt</option>
          <option value="SV">El Salvador</option>
          <option value="GQ">Equatorial Guinea</option>
          <option value="ER">Eritrea</option>
          <option value="EE">Estonia</option>
          <option value="ET">Ethiopia</option>
          <option value="FK">Falkland Islands (Malvinas)</option>
          <option value="FO">Faroe Islands</option>
          <option value="FJ">Fiji</option>
          <option value="FI">Finland</option>
          <option value="FR">France</option>
          <option value="GF">French Guiana</option>
          <option value="PF">French Polynesia</option>
          <option value="TF">French Southern Territories</option>
          <option value="GA">Gabon</option>
          <option value="GM">Gambia</option>
          <option value="GE">Georgia</option>
          <option value="DE">Germany</option>
          <option value="GH">Ghana</option>
          <option value="GI">Gibraltar</option>
          <option value="GR">Greece</option>
          <option value="GL">Greenland</option>
          <option value="GD">Grenada</option>
          <option value="GP">Guadeloupe</option>
          <option value="GU">Guam</option>
          <option value="GT">Guatemala</option>
          <option value="GG">Guernsey</option>
          <option value="GN">Guinea</option>
          <option value="GW">Guinea-Bissau</option>
          <option value="GY">Guyana</option>
          <option value="HT">Haiti</option>
          <option value="HM">Heard Island and Mcdonald Islands</option>
          <option value="VA">Holy See (Vatican City State)</option>
          <option value="HN">Honduras</option>
          <option value="HK">Hong Kong</option>
          <option value="HU">Hungary</option>
          <option value="IS">Iceland</option>
          <option value="IN">India</option>
          <option value="ID">Indonesia</option>
          <option value="IR">Iran, Islamic Republic of</option>
          <option value="IQ">Iraq</option>
          <option value="IE">Ireland</option>
          <option value="IM">Isle of Man</option>
          <option value="IL">Israel</option>
          <option value="IT">Italy</option>
          <option value="JM">Jamaica</option>
          <option value="JP">Japan</option>
          <option value="JE">Jersey</option>
          <option value="JO">Jordan</option>
          <option value="KZ">Kazakhstan</option>
          <option value="KE">Kenya</option>
          <option value="KI">Kiribati</option>
          <option value="KP">Korea, Democratic People's Republic of</option>
          <option value="KR">Korea, Republic of</option>
          <option value="XK">Kosovo</option>
          <option value="KW">Kuwait</option>
          <option value="KG">Kyrgyzstan</option>
          <option value="LA">Lao People's Democratic Republic</option>
          <option value="LV">Latvia</option>
          <option value="LB">Lebanon</option>
          <option value="LS">Lesotho</option>
          <option value="LR">Liberia</option>
          <option value="LY">Libyan Arab Jamahiriya</option>
          <option value="LI">Liechtenstein</option>
          <option value="LT">Lithuania</option>
          <option value="LU">Luxembourg</option>
          <option value="MO">Macao</option>
          <option value="MK">Macedonia, the Former Yugoslav Republic of</option>
          <option value="MG">Madagascar</option>
          <option value="MW">Malawi</option>
          <option value="MY">Malaysia</option>
          <option value="MV">Maldives</option>
          <option value="ML">Mali</option>
          <option value="MT">Malta</option>
          <option value="MH">Marshall Islands</option>
          <option value="MQ">Martinique</option>
          <option value="MR">Mauritania</option>
          <option value="MU">Mauritius</option>
          <option value="YT">Mayotte</option>
          <option value="MX">Mexico</option>
          <option value="FM">Micronesia, Federated States of</option>
          <option value="MD">Moldova, Republic of</option>
          <option value="MC">Monaco</option>
          <option value="MN">Mongolia</option>
          <option value="ME">Montenegro</option>
          <option value="MS">Montserrat</option>
          <option value="MA">Morocco</option>
          <option value="MZ">Mozambique</option>
          <option value="MM">Myanmar</option>
          <option value="NA">Namibia</option>
          <option value="NR">Nauru</option>
          <option value="NP">Nepal</option>
          <option value="NL">Netherlands</option>
          <option value="AN">Netherlands Antilles</option>
          <option value="NC">New Caledonia</option>
          <option value="NZ">New Zealand</option>
          <option value="NI">Nicaragua</option>
          <option value="NE">Niger</option>
          <option value="NG">Nigeria</option>
          <option value="NU">Niue</option>
          <option value="NF">Norfolk Island</option>
          <option value="MP">Northern Mariana Islands</option>
          <option value="NO">Norway</option>
          <option value="OM">Oman</option>
          <option value="PK">Pakistan</option>
          <option value="PW">Palau</option>
          <option value="PS">Palestinian Territory, Occupied</option>
          <option value="PA">Panama</option>
          <option value="PG">Papua New Guinea</option>
          <option value="PY">Paraguay</option>
          <option value="PE">Peru</option>
          <option value="PH">Philippines</option>
          <option value="PN">Pitcairn</option>
          <option value="PL">Poland</option>
          <option value="PT">Portugal</option>
          <option value="PR">Puerto Rico</option>
          <option value="QA">Qatar</option>
          <option value="RE">Reunion</option>
          <option value="RO">Romania</option>
          <option value="RU">Russian Federation</option>
          <option value="RW">Rwanda</option>
          <option value="BL">Saint Barthelemy</option>
          <option value="SH">Saint Helena</option>
          <option value="KN">Saint Kitts and Nevis</option>
          <option value="LC">Saint Lucia</option>
          <option value="MF">Saint Martin</option>
          <option value="PM">Saint Pierre and Miquelon</option>
          <option value="VC">Saint Vincent and the Grenadines</option>
          <option value="WS">Samoa</option>
          <option value="SM">San Marino</option>
          <option value="ST">Sao Tome and Principe</option>
          <option value="SA">Saudi Arabia</option>
          <option value="SN">Senegal</option>
          <option value="RS">Serbia</option>
          <option value="CS">Serbia and Montenegro</option>
          <option value="SC">Seychelles</option>
          <option value="SL">Sierra Leone</option>
          <option value="SG">Singapore</option>
          <option value="SX">Sint Maarten</option>
          <option value="SK">Slovakia</option>
          <option value="SI">Slovenia</option>
          <option value="SB">Solomon Islands</option>
          <option value="SO">Somalia</option>
          <option value="ZA">South Africa</option>
          <option value="GS">
            South Georgia and the South Sandwich Islands
          </option>
          <option value="SS">South Sudan</option>
          <option value="ES">Spain</option>
          <option value="LK">Sri Lanka</option>
          <option value="SD">Sudan</option>
          <option value="SR">Suriname</option>
          <option value="SJ">Svalbard and Jan Mayen</option>
          <option value="SZ">Swaziland</option>
          <option value="SE">Sweden</option>
          <option value="CH">Switzerland</option>
          <option value="SY">Syrian Arab Republic</option>
          <option value="TW">Taiwan, Province of China</option>
          <option value="TJ">Tajikistan</option>
          <option value="TZ">Tanzania, United Republic of</option>
          <option value="TH">Thailand</option>
          <option value="TL">Timor-Leste</option>
          <option value="TG">Togo</option>
          <option value="TK">Tokelau</option>
          <option value="TO">Tonga</option>
          <option value="TT">Trinidad and Tobago</option>
          <option value="TN">Tunisia</option>
          <option value="TR">Turkey</option>
          <option value="TM">Turkmenistan</option>
          <option value="TC">Turks and Caicos Islands</option>
          <option value="TV">Tuvalu</option>
          <option value="UG">Uganda</option>
          <option value="UA">Ukraine</option>
          <option value="AE">United Arab Emirates</option>
          <option value="GB">United Kingdom</option>
          <option value="US">United States</option>
          <option value="UM">United States Minor Outlying Islands</option>
          <option value="UY">Uruguay</option>
          <option value="UZ">Uzbekistan</option>
          <option value="VU">Vanuatu</option>
          <option value="VE">Venezuela</option>
          <option value="VN">Viet Nam</option>
          <option value="VG">Virgin Islands, British</option>
          <option value="VI">Virgin Islands, U.s.</option>
          <option value="WF">Wallis and Futuna</option>
          <option value="EH">Western Sahara</option>
          <option value="YE">Yemen</option>
          <option value="ZM">Zambia</option>
          <option value="ZW">Zimbabwe</option>
        </select>
        <label for="zipCode" class="zipCode">Postal / Zip Code</label>
        <input
          type="text"
          name="zipCode"
          id="zipCode"
          required
          v-model="formValues.zipCode"
        />
      </div>
      <hr style="margin: 35px 0" />

      <h2 style="text-align: center">Travel Details</h2>
      <div class="travelDetails">
        <div class="travelDate">
          <label class="dateDetail" for="dateDetail">Travel Date:</label>
          <input
            type="date"
            id="dateDetail"
            name="date"
            v-model="formValues.travelDate"
          />
        </div>
        <div class="destination">
          <label class="destinationTitle" for="destination"
            >Choice destination:</label
          >
          <select
            name="destination"
            id="destination"
            multiple
            v-model="formValues.destination"
          >
            <option value="">Select country</option>
            <option value="Paris">Paris</option>
            <option value="New Zeland">New Zeland</option>
            <option value="Maui">Maui</option>
            <option value="Bora Bora">Bora Bora</option>
            <option value="Tahity">Tahity</option>
            <option value="London">London</option>
            <option value="Holand">Holand</option>
            <option value="Kanada">Kanada</option>
            <option value="USA">USA</option>
            <option value="Swizerland">Swizerland</option>
            <option value="Austria">Austria</option>
            <option value="Czech Republic">Czech Republic</option>
            <option value="Italia">Italia</option></select
          ><br />
          (ctrl + mouseClick for select more)
        </div>
      </div>
      <hr style="margin: 35px 0" />

      <h2>Type of Trip</h2>
      <div class="type-of-trip">
        <label for="honeymoon">Honeymoon</label>
        <input
          type="radio"
          id="honeymoon"
          name="honeymoon"
          value="honeymoon"
          v-model="formValues.typeOfTrip"
        />
        <label for="business">Business</label>
        <input
          type="radio"
          id="business"
          name="business"
          value="business"
          v-model="formValues.typeOfTrip"
        />
        <label for="familyVocation">Family Volation</label>
        <input
          type="radio"
          id="familyVocation"
          name="familyVocation"
          value="familyVocation"
          v-model="formValues.typeOfTrip"
        />
        <label for="other">Other</label>
        <input
          type="radio"
          id="other"
          name="other"
          value="other"
          v-model="formValues.typeOfTrip"
        />
      </div>
      <h2>Other Services Needed</h2>
      <div class="type-of-trip">
        <label for="Flights">Flights Only</label>
        <input
          type="checkbox"
          id="Flights"
          name="Flights"
          value="Flights"
          v-model="formValues.flightOnly"
          true-value="yes"
          false="no"
        />
        <label for="rental-car">Rental Car</label>
        <input
          type="checkbox"
          id="rental-car"
          name="rental-car"
          value="rental-car"
          v-model="formValues.rentalCar"
          true-value="yes"
          false-value="no"
        />
        <label for="entertainment">entertainment</label>
        <input
          type="checkbox"
          id="entertainment"
          name="entertainment"
          value="entertainment"
          v-model="formValues.entertainment"
          true-value="yes"
          false-value="no"
        />
        <label for="Hotel">Hotel / Resorts</label>
        <input
          type="checkbox"
          id="Hotel"
          name="Hotel"
          value="Hotel"
          v-model="formValues.hotel"
          true-value="yes"
          false-value="no"
        />
      </div>
      <hr style="margin: 35px 0" />
      <h2>Credit Card</h2>
      <div class="cardDetails">
        <label for="creaditCard">Creadit card number:</label>
        <input
          type="text"
          id="creaditCard"
          name="firstNameCard"
          placeholder="Enter card number"
          v-model="formValues.cardNumber"
        />
        <label for="creaditCardname">Creadit card name:</label>
        <input
          type="text"
          id="creaditCard"
          name="firstNameCard"
          placeholder="Enter card number"
          v-model="formValues.cardName"
        />
        <button>Submit</button>
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
        firstName: "",
        lastName: "",
        date: "",
        eMail: "",
        phoneNumber: "",
        adreseStreet1: "",
        adreseStreet2: "",
        city: "",
        state: "",
        country: "",
        zipCode: "",
        travelDate: "",
        destination: [],
        typeOfTrip: [],
        flightOnly: "no",
        rentalCar: "no",
        entertainment: "no",
        hotel: "no",
        cardNumber: "",
        cardName: "",
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
  background-color: rgb(233, 230, 230);
}
form {
  width: 750px;
  margin: 10px auto;
}
label + input {
  font-weight: bold;
  margin: 0 5px;
}
label {
  font-weight: bold;
}
input[type="text"] {
  font-size: 14px;
  color: #555;
  border-radius: 3px;
  border: 1px solid rgb(151, 150, 150);
}
.form-name,
.form-example,
.form-adrese,
.form-city,
.travelDetails,
.destination {
  margin: 15px 0;
}
#firstName,
#lastName {
  width: 110px;
  height: 30px;
}
.lastName {
  margin-left: 15px;
}
#date {
  margin-left: 15px;
  width: 191px !important;
}
.form-name > .date {
  margin-left: 20px !important;
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
  margin-right: 35px;
}
.phoneNumber {
  margin-left: 70px;
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
  margin-left: 135px;
}
.zipCode {
  margin-left: 130px;
}
#zipCode {
  width: 170px;
}

.city {
  margin-right: 65px;
}
#country {
  width: 170px;
  margin-left: 37px;
}
.form-city {
  margin-top: 15px;
}
.form-city #city,
.form-city #state {
  width: 170px;
}
#creaditCard {
  display: inline-block;
  width: 150px;
  height: 30px;
}
.travelDetails {
  display: inline-flex;
  justify-content: space-between;
  width: 710px;
}
.travelDate {
  width: 250px;
}
#dateDetail {
  width: 200px;
}
.destination {
  /* display: block; */
  width: 250px;
  color: rgb(26, 23, 23);
  padding-left: 50px;
  margin-top: 0px;
}
.cardDetails > button {
  display: block;
  margin: 20px auto;
  justify-content: center;
  background-color: rgb(112, 210, 235);
  padding: 10px 15px;
  width: 150px;
  color: rgb(87, 66, 66);
  font-size: 25px;
  font-weight: 600;
}
#destination {
  width: 150px;
  height: 150px;
  text-align: start;
  padding-left: 15px;
  /* display: inline-flex; */
}
</style>
