<template>
  <div class="retro-console">
    <p v-for="o in output" v-bind:key="o" >{{o}}</p>
  </div>
</template>

<script>
export default {
  name: 'RetroConsole',
  props: {
    output: Array,
    fontSize: {
      type: Number,
      default: 12
    },
    consoleSize: {
      type: Object,
      default: () => ({
        height: '150px',
        width: '100%'
      })
    },
    fullscreen: {
      type: Boolean,
      default: false
    }
  }
}
</script>

<style lang="scss" scoped>
.retro-console {
  color: limegreen;
  background-color: black;
  font-family: monospace;
  font-weight: bold;
  line-height: 1.1;
  font-size: 10vh;
  text-shadow: 0px 0px 6px limegreen;
}
.fullscreen {
  height: 100vh;
}
</style>
