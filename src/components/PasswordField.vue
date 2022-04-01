<template>
    <div>
        <div class="form-group">
            <div class="form-control">
                <input placeholder=" " :type="passwordType" @change="validatePassword" v-model="password">
                <label>Password</label>
            </div>
        </div>
        <div class="form">
            <img :src="minCharSrc" class="svg-icon" alt=""> {{ minchar }} Characters min.
            <img :src="minNumSrc" class="svg-icon" alt=""> One number
        </div>
    </div>
</template>

<script>
export default {
    name: "PasswordField",
    data() {
      return {
        password: "",
        passwordType: "password",
        minCharSrc: "assets/circle-check-solid-gray.svg",
        minNumSrc: "assets/circle-check-solid-gray.svg",
      }
    },
    props: {
        minchar: Number
    },
    methods: {
      showPassword() {
        this.passwordType = this.passwordType === "password" ? "text" : "password"
      },
      validatePassword() {
        ( this.password.length >= 8 ? this.minCharSrc = "assets/circle-check-solid.svg" : this.minCharSrc = "assets/circle-check-solid-gray.svg" )
        
        if ( /\d/.test(this.password) ) {
          this.minNumSrc = "assets/circle-check-solid.svg"
        }
        else {
          this.minNumSrc = "assets/circle-check-solid.svg"
        }
      }
    }
}
</script>

<style>

</style>