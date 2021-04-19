<template>
<calculate/>
</template>

<script>
import Calculate from "./components/calculate.vue"

export default {
  name: 'App',
  components: {
    Calculate,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #000000;
  margin-top: 300px;
  font-size: 25px;
}
</style>
