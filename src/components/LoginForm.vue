<template>
  <div class="container">

    <div class="form-container">
      <div class="back-container">
        <span class="back-button"> <img src="assets/arrow-left-solid.svg" class="svg-icon" alt="">  Back</span>
      </div>

      <div class="login-container">

        <SSO />

        <p>Or use your email for registration</p>

        <form @submit.prevent="">
          <div class="form-group">
              <InputField type="text" placeholder="First Name" />
              <InputField type="text" placeholder="Last Name" />
          </div>

          <div class="form-group">
            <InputField type="email" placeholder="Email" />
          </div>


          <PasswordField minchar="8" />

          <div class="form-group">
            <input type="checkbox" name="privacy-policy">
            <span>By creating account, you agree to accept our <a href="javascript:void(0)">Privacy Policy</a>, <a href="javascript:void(0)">Terms of Service</a> and <a href="javascript:void(0)">Notification settings</a>.</span>
          </div>

          <div class="form-group">
            <a class="btn">Create a Free Account!</a>
          </div>

          <p class="center-text gray-text">Already have an account? <a href="javascript:void(0)">Log in</a></p>
        </form>
      
      </div>

    </div>
    
  </div>
</template>

<script>
import SSO from "./SSO"
import InputField from "./InputField"
import PasswordField from "./PasswordField"

export default {
    name: "LoginForm",
    components: {
      SSO,
      InputField,
      PasswordField
    }
}
</script>

<style>

p, span {
  font-weight: bold;
}

.svg-icon {
  width: 15px;
  height: 15px;
}

.container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  justify-items: center;
}

.form-container {
  border: 1px solid none;
  border-radius: 10px;
  background-color: white;

  padding: 1em;
}

.form-group {
  display: flex;
  flex-direction: row;
  gap: 1em;
  padding: 10px 0;
}

.form-control {
  display: block;
  width: 100%;
  padding: 15px 10px 5px 10px;
  background-color: #F1F5FF;
  border: 1px solid white;
  border-radius: 5px;
}

.form-control input {
  background-color: rgba(241,245,255, 0);
  font-weight: bold;
  font-size: 15px;
  border: none;
  padding: 10px 0;
  position: relative;
  z-index: 2;
  width: 100%;
}

input:focus {
  outline: none;
}

label {
  display: block;
  font-size: 12px;
  font-weight: bold;

  color: #999;
  transform: translate(0.25rem, -1.5rem);
  transition: all 0.2s ease-out;

  position: relative;
  z-index: 1;
}

input:not(:placeholder-shown) + label {
  color: #111;
  transform: translate(0, -2.75rem);
  font-weight: initial;
}


.btn {
  background-color: #3C71FF;
  border: 1px solid none;
  border-radius: 5px;
  width: 100%;
  padding: 1em;
  text-align: center;
  color: white;
}

.btn:hover, .sso-group:hover {
  box-shadow: 0px 10px 10px rgba(128, 128, 128, 0.4);
  cursor: pointer;
}

.back-container {
    height: 30px;
}

.back-container span:hover{
  border-bottom: 2px solid blue;
  font-weight: bolder;
}

.center-text {
  text-align: center;
}

.gray-text {
  color: rgb(168, 167, 167);
}

@media (min-width:801px) { 
  /* big landscape tablets, laptops, and desktops */
  .form-container { width: 45%; margin: 1em; }
  .login-container { padding: 1em 4em }
}

</style>