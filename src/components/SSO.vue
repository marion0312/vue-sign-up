<template>
  <div>
      <p>Start from free</p>
      <h1>Create an account</h1>
      <div class="sso-container">
        <div class="sso-group">
            <svg class="icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 488 512">! Font Awesome Pro 6.1.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc.<path d="M488 261.8C488 403.3 391.1 504 248 504 110.8 504 0 393.2 0 256S110.8 8 248 8c66.8 0 123 24.5 166.3 64.9l-67.5 64.9C258.5 52.6 94.3 116.6 94.3 256c0 86.5 69.1 156.6 153.7 156.6 98.2 0 135-70.4 140.8-106.9H248v-85.3h236.1c2.3 12.7 3.9 24.9 3.9 41.4z"/></svg>
            <p>Sign up with Google</p>
        </div>
        <div class="sso-group">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 320 512">! Font Awesome Pro 6.1.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc.<path d="M279.14 288l14.22-92.66h-88.91v-60.13c0-25.35 12.42-50.06 52.24-50.06h40.42V6.26S260.43 0 225.36 0c-73.22 0-121.08 44.38-121.08 124.72v70.62H22.89V288h81.39v224h100.17V288z"/></svg>
            <p>Sign up with Facebook</p>
        </div>
      </div>
  </div>
</template>

<script>
export default {
    App: "SSO"
}
</script>

<style scoped>
.sso-container {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1em;
    justify-items: start;
}

.sso-group {
    height: 50px;
    width: 100%;
    display: flex;
    flex-direction: row;
    align-items: center;
    border: 1px solid #9DB8FF;
    border-radius: 5px;
}

.sso-group svg{
    /* height: 100px; */
    height: 50%;
    width: 20%;
}

path {
    fill: #3C71FF;
}

p {
    font-weight: bold;
}

.sso-group:hover {
    background-color: #3C71FF;
    color: white;
    fill: white;
    cursor: pointer;
}

.sso-group:hover svg path {
    fill: white;
}
</style>