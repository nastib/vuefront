<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/vue.svg" style="height: 100px; width: 100px;">
    <ReadJSON/>
  </div>
</template>
<script setup lang="ts">
import ReadJSON from './components/ReadJSON.vue'
</script>
<style>

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>