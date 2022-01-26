<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <Signupform title="Demo App"/>
</template>

<script>
import Signupform from './components/Signupform'

export default {
  name: 'App',
  data() {
    return {
    title: 'Demo App'
    }
  },
  components: {      
    Signupform
  }
}
</script>

<style>
#app {
  text-align: center;
  margin-top: 60px;
}
</style>
