<template>
  <div id="app">
      <layout></layout>
  </div>
</template>

<script>
import layout from './components/Layout'

export default {
  name: 'app',
  components: {
    layout
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  font-size: 14px;
   -webkit-print-color-adjust: exact;
}

@media screen {
  #app {
    margin-top: 60px;
  }
}

</style>
