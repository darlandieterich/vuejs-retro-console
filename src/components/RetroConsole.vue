<template>
  <div class="retro-console" v-bind:class="{fullscreen: fullscreen}" :style="`${getStyle} font-size:${fontSize}px`">
    {{getStyle}}
    <div v-for="o in output" v-bind:key="o" >{{o}}</div>
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
        height: '250px',
        width: '50%'
      })
    },
    fullscreen: {
      type: Boolean,
      default: false
    }
  },
  data () {
    return {
      color: 'red' 
    }
  },
  computed: {
    getStyle: function () {
      return Object.entries(this.consoleSize).map(function (key) {
        return `${key[0]}:${key[1]}`
      }).join(";")+";"
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
  font-size: 20px;
  text-shadow: 0px 0px 6px limegreen;
}
.fullscreen {
  position: absolute;
  height: 100vh;
  
}
</style>
