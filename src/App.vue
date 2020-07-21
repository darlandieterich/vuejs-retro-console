<template>
  <div id="app">
    <RetroConsole :output="['blash', 'main', 'consolO']" :fullscreen="true"/>
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
</style>
