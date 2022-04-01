<template>
  <div>
    <LoginForm />
  </div>
</template>

<script>
import LoginForm from './components/LoginForm.vue'

export default {
  name: 'App',
  components: {
    LoginForm,
  }
}
</script>

<style>
body {
  background: #F1F5FF;
  font-family: 'Roboto';
  padding: 0;
  margin: 0;
}

</style>
