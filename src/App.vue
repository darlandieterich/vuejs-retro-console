<template>
  <div id="app">
    <h2>Example</h2>    
    <input type="text" ref="fieldx" v-model="value" v-on:keyup.enter="insere">
    <RetroConsole :output="lines" :fullscreen="false" :fontSize="15" :consoleSize="{height:'100px',width:'50%'}"/>
  </div>
</template>

<script>
import RetroConsole from './RetroConsole'

export default {
  name: 'App',
  components: {
    RetroConsole
  },
  data () {
    return {
      lines: ['one', 'two', 'three'],
      value: ''
    }
  },
  methods: {
    insere () {
      this.lines.push(this.value)
      this.value = ''
    }
  }
}
</script>

<style>
body {
  margin: 0px;
  padding: 0px;
}
</style>
