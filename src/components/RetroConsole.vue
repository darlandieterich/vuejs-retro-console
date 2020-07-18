<template>
  <div class="retro-console">
    {{output}}    
  </div>
</template>

<script>
export default {
  name: 'RetroConsole',
  props: {
    output: String
  }
}
</script>

<style scoped>
.retro-console {
  color: #2c3e50;
}
</style>
