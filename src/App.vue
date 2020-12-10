<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <Menu />
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import Menu from './components/Menu.vue';

export default defineComponent({
  name: 'App',
  components: {
    Menu,
  },
});
</script>

<style>
@import '/css/all.css';
@import './styles/main.css';

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
