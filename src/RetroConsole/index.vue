<template>
  <div class="retro-console" v-bind:class="{fullscreen: fullscreen}" :style="`font-size:${fontSize}px; ${getStyle}`">
    <div v-for="(o, idx) in output" v-bind:key="o+idx" >{{o}}</div>
    <slot></slot>
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
    styles: {
      type: Object,
      default: () => ({})
    },
    fullscreen: {
      type: Boolean,
      default: false
    }
  },
  computed: {
    getStyle: function () {
      return Object.entries(this.styles).map(function (key) {
        return `${key[0]}:${key[1]}`
      }).join(";")
    }
  }
}
</script>

<style lang="scss" scoped>
.retro-console {
  overflow: scroll;
  overflow-x: hidden;
  overflow-y: auto;
  color: limegreen;
  background-color: black;
  font-family: monospace;
  font-weight: bold;
  line-height: 1.1;
  font-size: 20px;
  text-shadow: 0px 0px 6px limegreen;
  border: 1px;
  border-style: solid;
  border-color: limegreen;
  padding: 0.25em;
}
.fullscreen {
  position: fixed;
  height: 100vh;
  width: 100%;
  height: 100%;
  left: 0;
  top: 0;
  z-index: 999;
}
</style>
