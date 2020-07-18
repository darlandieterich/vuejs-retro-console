<template>
  <div class="retro-console">
    <p v-for="o in output" v-bind:key="o">{{o}}</p>
  </div>
</template>

<script>
export default {
  name: 'RetroConsole',
  props: {
    output: Array
  }
}
</script>

<style scoped>
.retro-console {
  color: limegreen;
  background-color: black;
  font-family: monospace;
  font-weight: bold;
  line-height: 1.1;
  font-size: 10vh;
}
</style>
