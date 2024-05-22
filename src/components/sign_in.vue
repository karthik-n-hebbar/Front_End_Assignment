<template>
  <body>
    <div class="sign-in-container" v-cloak>
      <div class="contents">
        <div class="logo-container">
          <img class="logo" src="@/assets/Logo Container.png" alt="" />
        </div>
        <div class="signIn">Sign in</div>
        <form @submit="submitForm">
          <div class="email">
            <label for="email">Email</label><br />
            <input
              id="email"
              class="input-field"
              type="email"
              v-model="formValues.email"
              placeholder="Enter your email address"
              required
            />
          </div>
          <div class="password">
            <label for="password">Password</label><br />
            <input
              id="password"
              class="input-field"
              type="password"
              v-model="formValues.password"
              placeholder="Enter your password"
              required
            />
          </div>
          <div class="forgotPassword" v-on:click="forgotPasswordAlert">
            Forgot Password?
          </div>
          <div class="rememberMe">
            <input
              type="checkbox"
              v-model="formValues.Keep_me_signed_in"
              required
            />
            <label for="rememberMe">Keep me signed in for 30 days</label>
          </div>
          <button
            type="submit"
            v-on:click="
              submitForm();
              signInSuccessful();
            "
          >
            SIGN IN
          </button>
          <!-- <div class="signIn_button">
          </div> -->
        </form>
        <div class="tos">
          Read our Terms of Service
          <img src="@/assets/external-link.png" alt="" />
        </div>
      </div>
      <div class="bottomContainer">
        <div class="platforms">
          <div class="text_1">OTHER WAYS TO WATCH</div>
          <div class="platform_logos">
            <div class="logos">
              <img
                id="logo_1"
                src="@/assets/Group 24.png"
                style="width: 100%"
              />
            </div>
            <div class="logos">
              <img
                id="logo_2"
                src="@/assets/Group 23.png"
                style="width: 100%"
              />
            </div>
            <div class="logos">
              <img
                id="logo_3"
                src="@/assets/Group 25.png"
                style="width: 100%"
              />
            </div>
            <div class="logos">
              <img
                id="logo_4"
                src="@/assets/Group 22.png"
                style="width: 100%"
              />
            </div>
          </div>
          <div class="text_2">Search for AppleTV+ FYC on your App Store</div>
        </div>
      </div>
    </div>
  </body>
</template>

<script>
// import popUp from "./components/popUp.vue";
// import { ref } from "vue";

export default {
  name: "sign_in",
  components: {},
  //   setup() {
  //     const popupTriggers = ref({
  //       buttonTriggers: false,
  //     });

  //     const TogglePopUp = (trigger) => {
  //       popupTriggers.value[trigger] = !popupTriggers.value[trigger];
  //     };
  //     return {
  //       popUp,
  //       popupTriggers,
  //       TogglePopUp,
  //     };
  //   },
  data() {
    return {
      formValues: {
        email: "",
        password: "",
        Keep_me_signed_in: "",
      },
    };
  },
  methods: {
    submitForm() {
      //   event.preventDefault();
      console.log("User Input:", this.formValues);
    },
    forgotPasswordAlert() {
      alert(
        "A link has been sent to your registered Mail-Id to reset the password"
      );
    },
    signInSuccessful() {
      alert("Sign in Successful");
    },
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  background: linear-gradient(
      90deg,
      rgba(0, 0, 0, 0.52) 0%,
      rgba(0, 0, 0, 0) 84.31%
    ),
    url("@/assets/Netflix Movie Tile Background.png");
  background-repeat: repeat-y;
  background-attachment: fixed;
  background-size: cover;
  display: flex;
  width: auto;
  height: 100vh;
  justify-content: center;
  align-items: center;
}
body::before {
  content: "";
  position: absolute;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5);
}

.sign-in-container {
  position: relative;
  width: 100%;
  height: 88.4%;
  background: var(--Elements-Glass-Black, rgba(10, 10, 10, 1));
  border-radius: 15px;
  backdrop-filter: blur(10px);
  border-radius: 15px;
  border: 3px solid var(--Elements-Tamara-Black, rgba(24, 24, 24, 1));
  box-shadow: 10px 10px 15px 10px rgba(0, 0, 0, 0.25);
  opacity: 85%;
}
.contents {
  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  padding: 50px;
}
.contents div {
  display: block;
}
.logo-container {
  position: relative;
  width: 100%;
  height: auto;
  display: flex;
  justify-content: center;
  align-items: center;
}
.logo {
  max-height: 100%;
  max-width: 50%;
}
.signIn {
  font-family: Noto Sans;
  font-size: auto;
  font-weight: 600;
  line-height: 43.58px;
  text-align: left;
  color: white;
  width: 100%;
  height: 3.456%;
}

form {
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  width: 100%;
  height: auto;
}

.email,
.password,
.signIn_button {
  display: block;
  font-size: auto;
  color: var(--Type-Heroic-Blue, rgba(26, 104, 255, 1));
  width: 100%;
  height: 8.48%;
}
.email,
.password {
  font-family: Noto Sans;
  font-size: auto;
  font-weight: 600;
  line-height: 32.69px;
  text-align: left;
}
.input-field {
  width: 100%;
  height: 67.59%;
  outline: 0;
  border: 2px solid rgba(44, 44, 46, 1);
  background-color: rgba(28, 28, 30, 1);
  border: 2px solid rgba(44, 44, 46, 1);
  font-size: 15px;
  color: var(--Type-Gravel-Fint, rgba(188, 188, 188, 1));
  font-family: Noto Sans;
  font-size: auto;
  font-weight: 400;
  line-height: 32.69px;
  text-align: left;
  padding: 10px;
  padding-left: 15px;
}
.forgotPassword {
  text-align: right;
  color: white;
  font-family: Noto Sans;
  font-size: 75%;
  font-weight: 400;
  height: 1.57%;
  cursor: pointer;
  padding-top: 10px;
}
.rememberMe {
  color: white;
  font-family: Noto Sans;
  font-size: 75%;
  font-weight: 400;
  line-height: 27.24px;
  text-align: left;
  height: 2.83%;
}
.rememberMe input {
  margin-right: 10px;
}
button {
  color: white;
  font-family: Noto Sans;
  font-size: auto;
  font-weight: 600;
  line-height: 32.69px;
  letter-spacing: 4px;
  text-align: center;
  width: 100%;
  height: 8.48%;
  background: var(--Primary-Electric-Blue, rgba(0, 87, 255, 1));
  color: white;
  border: none;
  padding: 10px 20px;
  border-radius: 5px;
  cursor: pointer;
  font-size: auto;
  margin-top: 9.42%;
}
button::onclick {
  background: var(--Primary-Electric-Blue, rgb(17, 79, 202));
}
.tos {
  font-family: Noto Sans;
  font-size: auto;
  font-weight: 400;
  line-height: 30px;
  text-align: left;
  color: var(--Type-Gravel-Fint, rgba(188, 188, 188, 1));
  height: 1.256%;
  margin-top: 9.42%;
}
.bottomContainer {
  background-color: var(--Elements-Ebony-Gray, rgba(45, 49, 55, 1));
  position: absolute;
  bottom: 0;
  width: 100%;
  height: 21.45%;
  border-radius: 0px 0px 15px 15px;
}
.platforms {
  background-color: var(--Elements-Bunker-Gray, rgba(36, 39, 44, 1));
  position: absolute;
  bottom: 0;
  width: 100%;
  height: 72.16%;
  border-radius: 0px 0px 15px 15px;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  padding: 10px;
}
.text_1 {
  font-family: Noto Sans;
  font-size: 20%;
  font-weight: 700;
  letter-spacing: 0.14em;
  text-align: center;
  color: var(--Type-Silver-Medal, rgba(213, 213, 213, 1));
  margin-bottom: 5.56%;
}
.text_2 {
  font-family: Noto Sans;
  font-size: 20%;
  font-weight: 400;
  text-align: center;
  color: var(--Type-Silver-Medal, rgba(213, 213, 213, 1));
  margin-bottom: 10px;
}
.platform_logos {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 14.7%;
  gap: 10px;
  margin-bottom: 5%;
  margin-left: 18.6%;
  margin-right: 18.6%;
}
.platform_logos img {
  max-width: 50%;
  max-height: 50%;
}
</style>
