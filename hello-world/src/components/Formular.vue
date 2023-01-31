<template>
  <!-- <div>
    <pre>
      {{ JSON.stringify(formValues, null, 5) }}
    </pre>
  </div> -->

  <div class="fillTemplate">
    <ul>
      <li>First name:{{ formValues.firstName }}</li>
      <li>Last name:{{ formValues.lastName }}</li>
      <li>Birthdate:{{ formValues.date }}</li>
      <li>E-mail:{{ formValues.eMail }}</li>
      <li>Phone number:{{ formValues.phoneNumber }}</li>
      <li>Adresse 1:{{ formValues.adreseStreet1 }}</li>
      <li>Adresse 2:{{ formValues.adreseStreet2 }}</li>
      <li>City:{{ formValues.city }}</li>
      <li>State:{{ formValues.state }}</li>
      <li>Country:{{ formValues.country }}</li>
      <li>Zip code:{{ formValues.zipCode }}</li>
      <li>Date of travel:{{ formValues.travelDate }}</li>
      <li>Destination:{{ formValues.destination }}</li>
      <li>During of trip:{{ formValues.duringTrip }}</li>
      <li>Type of trip:{{ formValues.typeOfTrip }}</li>
      <li>Fligh only:{{ formValues.flightOnly }}</li>
      <li>Rent card:{{ formValues.rentalCar }}</li>
      <li>Entertainmet: {{ formValues.entertainment }}</li>
      <li>Hotel:{{ formValues.hotel }}</li>
      <li>Name of card:{{ formValues.cardName }}</li>
      <li>Card number:{{ formValues.cardNumber }}</li>
      <li>Card expire:{{ formValues.cardExpire }}</li>
      <li>Card secure:{{ formValues.cardSecure }}</li>
    </ul>
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
          <option>country</option>
          <option value="Afghanistan">Afghanistan</option>
          <option value="Aland Islands">Åland Islands</option>
          <option value="Albania">Albania</option>
          <option value="Algeria">Algeria</option>
          <option value="American Samoa">American Samoa</option>
          <option value="Andorra">Andorra</option>
          <option value="Angola">Angola</option>
          <option value="Anguilla">Anguilla</option>
          <option value="Antarctica">Antarctica</option>
          <option value="Antigua and Barbuda">Antigua & Barbuda</option>
          <option value="Argentina">Argentina</option>
          <option value="Armenia">Armenia</option>
          <option value="Aruba">Aruba</option>
          <option value="Australia">Australia</option>
          <option value="Austria">Austria</option>
          <option value="Azerbaijan">Azerbaijan</option>
          <option value="Bahamas">Bahamas</option>
          <option value="Bahrain">Bahrain</option>
          <option value="Bangladesh">Bangladesh</option>
          <option value="Barbados">Barbados</option>
          <option value="Belarus">Belarus</option>
          <option value="Belgium">Belgium</option>
          <option value="Belize">Belize</option>
          <option value="Benin">Benin</option>
          <option value="Bermuda">Bermuda</option>
          <option value="Bhutan">Bhutan</option>
          <option value="Bolivia">Bolivia</option>
          <option value="Bonaire, Sint Eustatius and Saba">
            Caribbean Netherlands
          </option>
          <option value="Bosnia and Herzegovina">Bosnia & Herzegovina</option>
          <option value="Botswana">Botswana</option>
          <option value="Bouvet Island">Bouvet Island</option>
          <option value="Brazil">Brazil</option>
          <option value="British Indian Ocean Territory">
            British Indian Ocean Territory
          </option>
          <option value="Brunei Darussalam">Brunei</option>
          <option value="Bulgaria">Bulgaria</option>
          <option value="Burkina Faso">Burkina Faso</option>
          <option value="Burundi">Burundi</option>
          <option value="Cambodia">Cambodia</option>
          <option value="Cameroon">Cameroon</option>
          <option value="Canada">Canada</option>
          <option value="Cape Verde">Cape Verde</option>
          <option value="Cayman Islands">Cayman Islands</option>
          <option value="Central African Republic">
            Central African Republic
          </option>
          <option value="Chad">Chad</option>
          <option value="Chile">Chile</option>
          <option value="China">China</option>
          <option value="Christmas Island">Christmas Island</option>
          <option value="Cocos (Keeling) Islands">
            Cocos (Keeling) Islands
          </option>
          <option value="Colombia">Colombia</option>
          <option value="Comoros">Comoros</option>
          <option value="Congo">Congo - Brazzaville</option>
          <option value="Congo, Democratic Republic of the Congo">
            Congo - Kinshasa
          </option>
          <option value="Cook Islands">Cook Islands</option>
          <option value="Costa Rica">Costa Rica</option>
          <option value="Cote D'Ivoire">Côte d’Ivoire</option>
          <option value="Croatia">Croatia</option>
          <option value="Cuba">Cuba</option>
          <option value="Curacao">Curaçao</option>
          <option value="Cyprus">Cyprus</option>
          <option value="Czech Republic">Czechia</option>
          <option value="Denmark">Denmark</option>
          <option value="Djibouti">Djibouti</option>
          <option value="Dominica">Dominica</option>
          <option value="Dominican Republic">Dominican Republic</option>
          <option value="Ecuador">Ecuador</option>
          <option value="Egypt">Egypt</option>
          <option value="El Salvador">El Salvador</option>
          <option value="Equatorial Guinea">Equatorial Guinea</option>
          <option value="Eritrea">Eritrea</option>
          <option value="Estonia">Estonia</option>
          <option value="Ethiopia">Ethiopia</option>
          <option value="Falkland Islands (Malvinas)">
            Falkland Islands (Islas Malvinas)
          </option>
          <option value="Faroe Islands">Faroe Islands</option>
          <option value="Fiji">Fiji</option>
          <option value="Finland">Finland</option>
          <option value="France">France</option>
          <option value="French Guiana">French Guiana</option>
          <option value="French Polynesia">French Polynesia</option>
          <option value="French Southern Territories">
            French Southern Territories
          </option>
          <option value="Gabon">Gabon</option>
          <option value="Gambia">Gambia</option>
          <option value="Georgia">Georgia</option>
          <option value="Germany">Germany</option>
          <option value="Ghana">Ghana</option>
          <option value="Gibraltar">Gibraltar</option>
          <option value="Greece">Greece</option>
          <option value="Greenland">Greenland</option>
          <option value="Grenada">Grenada</option>
          <option value="Guadeloupe">Guadeloupe</option>
          <option value="Guam">Guam</option>
          <option value="Guatemala">Guatemala</option>
          <option value="Guernsey">Guernsey</option>
          <option value="Guinea">Guinea</option>
          <option value="Guinea-Bissau">Guinea-Bissau</option>
          <option value="Guyana">Guyana</option>
          <option value="Haiti">Haiti</option>
          <option value="Heard Island and Mcdonald Islands">
            Heard & McDonald Islands
          </option>
          <option value="Holy See (Vatican City State)">Vatican City</option>
          <option value="Honduras">Honduras</option>
          <option value="Hong Kong">Hong Kong</option>
          <option value="Hungary">Hungary</option>
          <option value="Iceland">Iceland</option>
          <option value="India">India</option>
          <option value="Indonesia">Indonesia</option>
          <option value="Iran, Islamic Republic of">Iran</option>
          <option value="Iraq">Iraq</option>
          <option value="Ireland">Ireland</option>
          <option value="Isle of Man">Isle of Man</option>
          <option value="Israel">Israel</option>
          <option value="Italy">Italy</option>
          <option value="Jamaica">Jamaica</option>
          <option value="Japan">Japan</option>
          <option value="Jersey">Jersey</option>
          <option value="Jordan">Jordan</option>
          <option value="Kazakhstan">Kazakhstan</option>
          <option value="Kenya">Kenya</option>
          <option value="Kiribati">Kiribati</option>
          <option value="Korea, Democratic People's Republic of">
            North Korea
          </option>
          <option value="Korea, Republic of">South Korea</option>
          <option value="Kosovo">Kosovo</option>
          <option value="Kuwait">Kuwait</option>
          <option value="Kyrgyzstan">Kyrgyzstan</option>
          <option value="Lao People's Democratic Republic">Laos</option>
          <option value="Latvia">Latvia</option>
          <option value="Lebanon">Lebanon</option>
          <option value="Lesotho">Lesotho</option>
          <option value="Liberia">Liberia</option>
          <option value="Libyan Arab Jamahiriya">Libya</option>
          <option value="Liechtenstein">Liechtenstein</option>
          <option value="Lithuania">Lithuania</option>
          <option value="Luxembourg">Luxembourg</option>
          <option value="Macao">Macao</option>
          <option value="Macedonia, the Former Yugoslav Republic of">
            North Macedonia
          </option>
          <option value="Madagascar">Madagascar</option>
          <option value="Malawi">Malawi</option>
          <option value="Malaysia">Malaysia</option>
          <option value="Maldives">Maldives</option>
          <option value="Mali">Mali</option>
          <option value="Malta">Malta</option>
          <option value="Marshall Islands">Marshall Islands</option>
          <option value="Martinique">Martinique</option>
          <option value="Mauritania">Mauritania</option>
          <option value="Mauritius">Mauritius</option>
          <option value="Mayotte">Mayotte</option>
          <option value="Mexico">Mexico</option>
          <option value="Micronesia, Federated States of">Micronesia</option>
          <option value="Moldova, Republic of">Moldova</option>
          <option value="Monaco">Monaco</option>
          <option value="Mongolia">Mongolia</option>
          <option value="Montenegro">Montenegro</option>
          <option value="Montserrat">Montserrat</option>
          <option value="Morocco">Morocco</option>
          <option value="Mozambique">Mozambique</option>
          <option value="Myanmar">Myanmar (Burma)</option>
          <option value="Namibia">Namibia</option>
          <option value="Nauru">Nauru</option>
          <option value="Nepal">Nepal</option>
          <option value="Netherlands">Netherlands</option>
          <option value="Netherlands Antilles">Curaçao</option>
          <option value="New Caledonia">New Caledonia</option>
          <option value="New Zealand">New Zealand</option>
          <option value="Nicaragua">Nicaragua</option>
          <option value="Niger">Niger</option>
          <option value="Nigeria">Nigeria</option>
          <option value="Niue">Niue</option>
          <option value="Norfolk Island">Norfolk Island</option>
          <option value="Northern Mariana Islands">
            Northern Mariana Islands
          </option>
          <option value="Norway">Norway</option>
          <option value="Oman">Oman</option>
          <option value="Pakistan">Pakistan</option>
          <option value="Palau">Palau</option>
          <option value="Palestinian Territory, Occupied">Palestine</option>
          <option value="Panama">Panama</option>
          <option value="Papua New Guinea">Papua New Guinea</option>
          <option value="Paraguay">Paraguay</option>
          <option value="Peru">Peru</option>
          <option value="Philippines">Philippines</option>
          <option value="Pitcairn">Pitcairn Islands</option>
          <option value="Poland">Poland</option>
          <option value="Portugal">Portugal</option>
          <option value="Puerto Rico">Puerto Rico</option>
          <option value="Qatar">Qatar</option>
          <option value="Reunion">Réunion</option>
          <option value="Romania">Romania</option>
          <option value="Russian Federation">Russia</option>
          <option value="Rwanda">Rwanda</option>
          <option value="Saint Barthelemy">St. Barthélemy</option>
          <option value="Saint Helena">St. Helena</option>
          <option value="Saint Kitts and Nevis">St. Kitts & Nevis</option>
          <option value="Saint Lucia">St. Lucia</option>
          <option value="Saint Martin">St. Martin</option>
          <option value="Saint Pierre and Miquelon">
            St. Pierre & Miquelon
          </option>
          <option value="Saint Vincent and the Grenadines">
            St. Vincent & Grenadines
          </option>
          <option value="Samoa">Samoa</option>
          <option value="San Marino">San Marino</option>
          <option value="Sao Tome and Principe">São Tomé & Príncipe</option>
          <option value="Saudi Arabia">Saudi Arabia</option>
          <option value="Senegal">Senegal</option>
          <option value="Serbia">Serbia</option>
          <option value="Serbia and Montenegro">Serbia</option>
          <option value="Seychelles">Seychelles</option>
          <option value="Sierra Leone">Sierra Leone</option>
          <option value="Singapore">Singapore</option>
          <option value="Sint Maarten">Sint Maarten</option>
          <option value="Slovakia">Slovakia</option>
          <option value="Slovenia">Slovenia</option>
          <option value="Solomon Islands">Solomon Islands</option>
          <option value="Somalia">Somalia</option>
          <option value="South Africa">South Africa</option>
          <option value="South Georgia and the South Sandwich Islands">
            South Georgia & South Sandwich Islands
          </option>
          <option value="South Sudan">South Sudan</option>
          <option value="Spain">Spain</option>
          <option value="Sri Lanka">Sri Lanka</option>
          <option value="Sudan">Sudan</option>
          <option value="Suriname">Suriname</option>
          <option value="Svalbard and Jan Mayen">Svalbard & Jan Mayen</option>
          <option value="Swaziland">Eswatini</option>
          <option value="Sweden">Sweden</option>
          <option value="Switzerland">Switzerland</option>
          <option value="Syrian Arab Republic">Syria</option>
          <option value="Taiwan, Province of China">Taiwan</option>
          <option value="Tajikistan">Tajikistan</option>
          <option value="Tanzania, United Republic of">Tanzania</option>
          <option value="Thailand">Thailand</option>
          <option value="Timor-Leste">Timor-Leste</option>
          <option value="Togo">Togo</option>
          <option value="Tokelau">Tokelau</option>
          <option value="Tonga">Tonga</option>
          <option value="Trinidad and Tobago">Trinidad & Tobago</option>
          <option value="Tunisia">Tunisia</option>
          <option value="Turkey">Turkey</option>
          <option value="Turkmenistan">Turkmenistan</option>
          <option value="Turks and Caicos Islands">
            Turks & Caicos Islands
          </option>
          <option value="Tuvalu">Tuvalu</option>
          <option value="Uganda">Uganda</option>
          <option value="Ukraine">Ukraine</option>
          <option value="United Arab Emirates">United Arab Emirates</option>
          <option value="United Kingdom">United Kingdom</option>
          <option value="United States">United States</option>
          <option value="United States Minor Outlying Islands">
            U.S. Outlying Islands
          </option>
          <option value="Uruguay">Uruguay</option>
          <option value="Uzbekistan">Uzbekistan</option>
          <option value="Vanuatu">Vanuatu</option>
          <option value="Venezuela">Venezuela</option>
          <option value="Viet Nam">Vietnam</option>
          <option value="Virgin Islands, British">
            British Virgin Islands
          </option>
          <option value="Virgin Islands, U.s.">U.S. Virgin Islands</option>
          <option value="Wallis and Futuna">Wallis & Futuna</option>
          <option value="Western Sahara">Western Sahara</option>
          <option value="Yemen">Yemen</option>
          <option value="Zambia">Zambia</option>
          <option value="Zimbabwe">Zimbabwe</option>
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
        <div class="howLong">
          <h3>During trip:</h3>
          <label for="2-4">2-4</label>
          <input
            type="radio"
            id="2-4"
            name="2-4"
            value="2-4"
            v-model="formValues.duringTrip"
          />
          <label for="5-8">5-8</label>
          <input
            type="radio"
            id="5-8"
            name="5-9"
            value="5-9"
            v-model="formValues.duringTrip"
          />
          <label for="9-15">9-15</label>
          <input
            type="radio"
            id="9-15"
            name="9-15"
            value="9-15"
            v-model="formValues.duringTrip"
          />
        </div>
      </div>
      <hr style="margin: 35px 0" />

      <h2 style="text-align: center">Payment Information</h2>
      <div class="cardDetails">
        <div class="creaditCardDetail">
          <label for="creaditCardname">Name</label>
          <input
            type="text"
            id="creaditCard"
            name="firstNameCard"
            placeholder="Enter card number"
            v-model="formValues.cardName"
          />
        </div>
        <div class="cardNumberInfo">
          <label for="creaditCard">Card Number</label>
          <input
            type="text"
            id="creaditCard"
            name="firstNameCard"
            placeholder="Enter card number"
            v-model="formValues.cardNumber"
          />
        </div>
        <div class="expirationDetail">
          <label for="expiration">Expiration (mm/yy)</label>
          <input
            type="text"
            id="expiration"
            name="expiration"
            placeholder="expiration"
            v-model="formValues.cardExpire"
          />
        </div>
        <div class="securityDetail">
          <label for="security">Security Code</label>
          <input
            type="text"
            id="security"
            name="security"
            placeholder=""
            v-model="formValues.cardSecure"
          />
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
        <label for="entertainment">entertainment:</label>
        <input
          type="checkbox"
          id="entertainment"
          name="entertainment"
          value="entertainment"
          v-model="formValues.entertainment"
          true-value="yes"
          false-value="no"
        />
        <label :for="Hotel">Hotel / Resorts</label>
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
      <button>Submit</button>
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
        destination: "",
        duringTrip: "",
        typeOfTrip: "",
        flightOnly: "no",
        rentalCar: "no",
        entertainment: "no",
        hotel: "no",
        cardName: "",
        cardNumber: "",
        cardExpire: "",
        cardSecure: "",
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
  width: 250px;
  color: rgb(26, 23, 23);
  padding-left: 50px;
  margin-top: 0px;
}
#destination {
  width: 150px;
  height: 150px;
  text-align: start;
  padding-left: 15px;
}
.cardDetails {
  width: 510px;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  margin: 0 auto;
}

.creaditCardDetail {
  width: 470px;
  margin: 0px auto;
}
#creaditCard {
  height: 50px;
  margin: 0 auto;
  width: 470px !important;
}
.cardNumberInfo {
  width: 470px;
  margin: 10px auto;
}

.expirationDetail {
  width: 230px;
  margin-top: 10px;
  margin-left: 20px;
}
#expiration {
  width: 230px;
  height: 50px;
  margin: 0 auto;
}
.securityDetail {
  width: 230px;
  margin-top: 10px;

  margin-right: 20px;
}
#security {
  width: 230px;
  height: 50px;
  margin: 0 auto;
}

.fillTemplate {
  width: 800px;
  height: 100%;
  background-color: rgb(70, 179, 243);
  margin: 50px auto;
  border-radius: 15px;
  box-shadow: 1px 1px 5px 3px rgb(146, 144, 144);
}
ul {
  padding: 25px 10px;
  margin: 10px auto;
  width: 750px;
  flex-wrap: wrap;
  display: flex;
  list-style-type: none;
}
li {
  font-weight: 300;
  color: rgb(248, 248, 248);
  font-size: 25px;
  flex-grow: 2;
  width: 270px;
  text-decoration: underline;
  padding-left: 20px;
}
li:nth-of-type(1) {
  flex-grow: 3;
  width: 230px;
}
li:nth-of-type(2) {
  flex-grow: 3;
  width: 150px;
}
li:nth-of-type(3) {
  flex-grow: 3;
  width: 130px;
  padding-bottom: 5px;
}
li:nth-of-type(4) {
  flex-grow: 2;
  width: 230px;
  padding-bottom: 5px;
}
li:nth-of-type(5) {
  flex-grow: 2;
  width: 250px;
  padding-bottom: 5px;
}
li:nth-of-type(6) {
  flex-grow: 7;
  width: 100%;
  padding-bottom: 5px;
}
li:nth-of-type(7) {
  flex-grow: 8;
  width: 100%;
  padding-bottom: 5px;
}
li:nth-of-type(8) {
  flex-grow: 2;
  width: 350px;
  padding-bottom: 5px;
}
li:nth-of-type(9) {
  flex-grow: 2;
  width: 350px;
  padding-bottom: 5px;
}
li:nth-of-type(10) {
  flex-grow: 2;
  width: 280px;
  padding-bottom: 50px;
}
li:nth-of-type(12) {
  flex-grow: 2;
  width: 300px;
  padding-bottom: 5px;
}
li:nth-of-type(13) {
  flex-grow: 2;
  width: 300px;
  padding-bottom: 5px;
}
li:nth-of-type(14) {
  flex-grow: 2;
  width: 352px;
  padding-bottom: 50px;
}
li:nth-of-type(15) {
  flex-grow: 2;
  width: 350px;
  padding-bottom: 5px;
}
li:nth-of-type(16) {
  flex-grow: 4;
  width: 160px;
  padding-bottom: 50px;
}
li:nth-of-type(17) {
  flex-grow: 4;
  width: 160px;
  padding-bottom: 5px;
}
li:nth-of-type(18) {
  flex-grow: 4;
  width: 185px;
  padding-bottom: 5px;
}
li:nth-of-type(19) {
  flex-grow: 4;
  width: 135px;
  padding-bottom: 5px;
}
</style>
