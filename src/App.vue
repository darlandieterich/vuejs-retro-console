<template>
  <div id="app">
    <RetroConsole :output="['blash', 'main', 'consolO']" :fullscreen="false" :fontSize="25"/>
  </div>
</template>

<script>
import RetroConsole from './components/RetroConsole.vue'

export default {
  name: 'App',
  components: {
    RetroConsole
  }
}
</script>

<style>
body {
  margin: 0px;
  padding: 0px;
}
</style>
