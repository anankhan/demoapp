<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <signupform/>
</template>

<script>
import signupform from './components/signupform.vue'

export default {
  name: 'App',
  components: {      
    signupform
  }
}
</script>

<style>
#app {
  text-align: center;
  margin-top: 60px;
}
</style>
